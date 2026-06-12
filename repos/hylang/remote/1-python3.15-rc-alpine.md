## `hylang:1-python3.15-rc-alpine`

```console
$ docker pull hylang@sha256:6d2d38736b16938de44b990eaffba35386c2e32af8a50818ca657eb41572015a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:1-python3.15-rc-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:fc0f01e9b4c2d443de9efa6a831f76354afc9edeb6676a35f8b345a7f798f281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7ad36586e6fac34b99025c636360303546437dc8d7a09995b2c56cd6e39b4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:38:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:38:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 10 Jun 2026 20:38:15 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 10 Jun 2026 20:38:15 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 10 Jun 2026 20:40:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 10 Jun 2026 20:40:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jun 2026 20:40:57 GMT
CMD ["python3"]
# Fri, 12 Jun 2026 00:02:45 GMT
ENV HY_VERSION=1.3.0
# Fri, 12 Jun 2026 00:02:45 GMT
ENV HYRULE_VERSION=1.1.0
# Fri, 12 Jun 2026 00:02:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 12 Jun 2026 00:02:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cdf273c2ec391f15155a4c8dc6eaa65ebdc5ca5f48e895e807f5fbb63418a9`  
		Last Modified: Wed, 10 Jun 2026 20:41:04 GMT  
		Size: 455.5 KB (455485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e540d5ff30540f8f3fb5ee658c64652d834907993f266197ce524ef2f7588587`  
		Last Modified: Wed, 10 Jun 2026 20:41:04 GMT  
		Size: 16.7 MB (16658913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350008ae4a141f811a13f1e481d392854075693cb08496661a5beeadf7dc906e`  
		Last Modified: Wed, 10 Jun 2026 20:41:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11b405b2a19ca603f10c85a710f7ad36d5e45ef8d05bc6b0ff47983d94dfd81`  
		Last Modified: Fri, 12 Jun 2026 00:02:51 GMT  
		Size: 5.8 MB (5844322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:2c18eededb0eb73d5d1f478cc06ea80c37c548c2815294e567cdf442eecc25f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0cfb2039b1dc406f96d6faa39264b3d51fe49455db47fd0286925522c45841`

```dockerfile
```

-	Layers:
	-	`sha256:59f5b18153ac2cda35bfeeef35df21579a8071d7ae4f7956a8aa4f24e0e21d13`  
		Last Modified: Fri, 12 Jun 2026 00:02:51 GMT  
		Size: 623.7 KB (623742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd87446a2cc8c73ea7a16b1066d9933b8f9f59b31d0b0937b8edb437d84314b5`  
		Last Modified: Fri, 12 Jun 2026 00:02:51 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9f0e4b16c72d5eba56aa8a0dcf07a27a97a5572f32f1dae787ed8910b985ac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27536842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ba89ccaaadcf08abdccda184754f14132987102452e1dabdc2fcf7e43b39a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:38:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:38:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 10 Jun 2026 20:38:33 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 10 Jun 2026 20:38:33 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 10 Jun 2026 20:41:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 10 Jun 2026 20:41:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jun 2026 20:41:17 GMT
CMD ["python3"]
# Fri, 12 Jun 2026 00:02:26 GMT
ENV HY_VERSION=1.3.0
# Fri, 12 Jun 2026 00:02:26 GMT
ENV HYRULE_VERSION=1.1.0
# Fri, 12 Jun 2026 00:02:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 12 Jun 2026 00:02:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935418fe18fb290c48519024194802f01da6404640053b02fbf75bd1b36bdf6b`  
		Last Modified: Wed, 10 Jun 2026 20:41:24 GMT  
		Size: 457.7 KB (457746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e388ec2de77af5f74f553d7adbbd429f6792147c950954ccd0dbcbb8ea19e2a9`  
		Last Modified: Wed, 10 Jun 2026 20:41:24 GMT  
		Size: 17.0 MB (17032278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c30898bf2927b7199bb52b8f42858750424f2222e42087ce9f770b77a4e9461`  
		Last Modified: Wed, 10 Jun 2026 20:41:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baf957f683da9418f0a9d63bfb8f07232085fe057bb9bcccc44a03ea3e9c1fb`  
		Last Modified: Fri, 12 Jun 2026 00:02:32 GMT  
		Size: 5.8 MB (5844239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:fa4895b6416ad5aa9e63423aeb4581f06072ff09add59ee9f470cba2dd4b9d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.8 KB (632751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a8ab9296c76a3a52c81aa3fb567058c727cb927b11ef1aaf02ccccd60c4c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18f886e3dd33bcf4812b1b356d6ada34b47d9a062383481c9e104a2a325d5e5`  
		Last Modified: Fri, 12 Jun 2026 00:02:32 GMT  
		Size: 623.2 KB (623196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eae625ce3be0a1e937ca0f700ed1c884196fc36f0bb21e837786994307ebe44`  
		Last Modified: Fri, 12 Jun 2026 00:02:32 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:98d7c36e4a334b28b684de267d2f3dfea2cccc02ca2d62e7ce2844c95eb668aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24039697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4f12c2e983c941f494b9526f757b582ab15d22f2d0adfa1692e9941632b9d6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 01:58:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 04 Jun 2026 02:41:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Jun 2026 02:41:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Jun 2026 02:41:13 GMT
CMD ["python3"]
# Tue, 09 Jun 2026 08:25:51 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 08:25:51 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 08:25:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Jun 2026 08:25:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765866854439454599b98b3453482041066c253a5bb4172d859d005f14f950ff`  
		Last Modified: Thu, 04 Jun 2026 02:41:58 GMT  
		Size: 455.8 KB (455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade6d6a20fcb68992a4db3b3eaff05ebd630ca6df0b614a6920cd066741543ff`  
		Last Modified: Thu, 04 Jun 2026 02:42:01 GMT  
		Size: 14.2 MB (14151047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571a66a89d3d5a8e1d5bdc7754da6cb0644ae7a963180b1224d5d48506890b7`  
		Last Modified: Thu, 04 Jun 2026 02:41:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b63de4bf424a883b9ce1c1b8e8430823921ffda6b0fcd8ff6dae29abe62baa1`  
		Last Modified: Tue, 09 Jun 2026 08:26:31 GMT  
		Size: 5.8 MB (5844908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:2b79ea0fb450a17ad23c0b0a56669d572ffaae764f14aea3476a1dd568e228a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.7 KB (632662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894f33df5a6c6b8b1481d59dd7975a3baa1a021e1fb0c1b2b1687e40182883d1`

```dockerfile
```

-	Layers:
	-	`sha256:ef2628fb0cce790483e28fb88ef3d573293880a83fa149e7da192e080eb72345`  
		Last Modified: Tue, 09 Jun 2026 08:26:30 GMT  
		Size: 623.2 KB (623191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c64497e671de9dfa6d4085bb2d7e8246bd8aeadfe1717b03091ebe35dd81f30`  
		Last Modified: Tue, 09 Jun 2026 08:26:30 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:29fbbe26f83e68618a3d86d22b4c237799b975adaf803c930775fbf2f583868c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26944649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd04f9182d2bda8d0a5004073024e3cc4253e22be462e7cd93bf7af73d0b3403`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:16:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 21:16:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 10 Jun 2026 21:16:54 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 10 Jun 2026 21:16:54 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 10 Jun 2026 21:22:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 10 Jun 2026 21:22:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jun 2026 21:22:12 GMT
CMD ["python3"]
# Fri, 12 Jun 2026 00:01:47 GMT
ENV HY_VERSION=1.3.0
# Fri, 12 Jun 2026 00:01:47 GMT
ENV HYRULE_VERSION=1.1.0
# Fri, 12 Jun 2026 00:01:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 12 Jun 2026 00:01:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2655cbe07b251b3337325c14f004ed35f22fcb8242405ece42c2591642bfec`  
		Last Modified: Wed, 10 Jun 2026 21:22:25 GMT  
		Size: 456.5 KB (456483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c87d905412d490d0e12f6ef6364bb09c21cf807477e714d89357e5412bc3a74`  
		Last Modified: Wed, 10 Jun 2026 21:22:25 GMT  
		Size: 16.9 MB (16913458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd9138d9d16001751532bd3b5f30cf5bdb8e0d95e79b206ae5696a91ac6471c`  
		Last Modified: Wed, 10 Jun 2026 21:22:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdb5a84ccf2c1bc994358c139bd4adbc68428ecc46b7ef8c759e08aba35a0db`  
		Last Modified: Fri, 12 Jun 2026 00:01:57 GMT  
		Size: 5.8 MB (5844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:1c4918e04046baa414313a5c24f910b028f0c3e91ec0d2f94e897c6f71ad1efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.5 KB (632494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2519796fd67964d0bdf4750fca677f0d67ae7950ae8b9f7b186c9b26650395`

```dockerfile
```

-	Layers:
	-	`sha256:2d832b2fba9ed4b0cc8380c1bb39b8c1b2ea13072eeb5325150852b1e8858d83`  
		Last Modified: Fri, 12 Jun 2026 00:01:57 GMT  
		Size: 623.1 KB (623091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f61106542e2e070bf6bf32e605995338f20ec2bae10788f01abb07d2b31cd65`  
		Last Modified: Fri, 12 Jun 2026 00:01:57 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json
