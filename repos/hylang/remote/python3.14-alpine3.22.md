## `hylang:python3.14-alpine3.22`

```console
$ docker pull hylang@sha256:ba168143994733cf4afc9e89430e835f1e74cefcb583dba3ce1c1a0334184d3e
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

### `hylang:python3.14-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:252e92ec09c27d61f19845dc00795ebfff5528c128429fec6c9e79807bd8e126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23357196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660c8d5d3051b4e0cffd75551eac00b69960c173fd4d96617045cdb800b95084`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:06:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:06:43 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:06:43 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:09:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:09:18 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:09:18 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:40 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f7e72420c2ec8ac67966fb4612dc5b68b57230a2613dbcc3b5bc2b55dff12e`  
		Last Modified: Mon, 11 May 2026 23:09:25 GMT  
		Size: 454.8 KB (454794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb8804f33d1ecf471765a351923fb93d8183f5ca9daf1e98e2c3c343447c211`  
		Last Modified: Mon, 11 May 2026 23:09:25 GMT  
		Size: 13.4 MB (13386591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8458e452702fbd8da1f7b3eec8ba10a4b0c4755d0fa409c41fd5440a192966`  
		Last Modified: Mon, 11 May 2026 23:09:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d254e238f2d4f99d05feda5d6aafc4be823c8b69c86db4839a0c8a80864fcb0`  
		Last Modified: Wed, 27 May 2026 00:11:46 GMT  
		Size: 5.7 MB (5707375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:f845796122f5738dd3ddde101ab3d2678c29fcac9654fb4c8ea9948bc4cac2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c30fd35b36d664bf07d9d610f1c690ffc7ff4571573645e651b602443e8d890`

```dockerfile
```

-	Layers:
	-	`sha256:cc222969fa94a47b9a0b10d012c56efa8f6eab4af34d15758fc6346f19c7e421`  
		Last Modified: Wed, 27 May 2026 00:11:46 GMT  
		Size: 625.0 KB (624953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2836407da5b6472630f5dd397326376c55a1a328a01c9ac90966ee8671f1bb`  
		Last Modified: Wed, 27 May 2026 00:11:45 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:f259c926a68f828a4c631867314de4057df757ee659cc6cd020575c17fb5518a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4791421ec85cf24fb99a59252d6d149058f8d82b38d580472438fa2b1dc821af`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:07:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:07:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:07:08 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:07:08 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:09:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:09:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:09:53 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:32 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:32 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef864e97c9d5cd82b4fbf501f48c38816dd5e5b85c3a46db536b176dbf72a6e`  
		Last Modified: Mon, 11 May 2026 23:09:58 GMT  
		Size: 455.7 KB (455724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1942518e1ab96a32c30b6f447ed704f61344df29a5b78dcfd83caa6ad22943e8`  
		Last Modified: Mon, 11 May 2026 23:09:59 GMT  
		Size: 13.0 MB (12975722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b81e6f285380f750417bfc2ff79c2760413bb1f54c5ce4d0a835b77dae010`  
		Last Modified: Mon, 11 May 2026 23:09:58 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41a0e66adff38cf0b01e3d68b613f998a1e1c8109b2ca6154f5ef0efe0e81bd`  
		Last Modified: Wed, 27 May 2026 00:10:36 GMT  
		Size: 5.7 MB (5707420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:43ff61484fc3ac60e26d671452a011390035c4d8d83189c80c0fbdcc074e8bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249471dea1f5b67bc3bc92eac8bf82334b1b32c8b4bd7c6f9ecbce8094da27a1`

```dockerfile
```

-	Layers:
	-	`sha256:3cab381f3bff0c19a90ce3b47fd7a8fc7c575d578edbb5a785e784c6641de01a`  
		Last Modified: Wed, 27 May 2026 00:10:36 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:35db90d173a20c8cde3deea0bb87dfb6b64fe696ee3940225fef5e1e244ca66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21981167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedd3ec2ac3dfbf3dc903274bdfa0f0bea1d9497b50b76a328a6d3e08e65bc79`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:10:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:10:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:10:22 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:10:22 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:13:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:13:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:13:10 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:14 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59afb6808742162410e9c8523b7c054bbce22c9b4cdbf0959bfaebf3597fe7d`  
		Last Modified: Mon, 11 May 2026 23:13:17 GMT  
		Size: 454.8 KB (454832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f967ce002a4c8cc1f0d32e91cb9063789f64c6ee8826f4339e060361f52f8744`  
		Last Modified: Mon, 11 May 2026 23:13:17 GMT  
		Size: 12.6 MB (12592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631e6b8368a4727229cffc2f9b25703a528f1359a7f80a114a1213284d59648a`  
		Last Modified: Mon, 11 May 2026 23:13:16 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6e8041fb747a5ab8c7f760b35ab88e0f4e2b4c7dcdb3caa9b98e7373f3f642`  
		Last Modified: Wed, 27 May 2026 00:11:20 GMT  
		Size: 5.7 MB (5707429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:7614d1e065bc1ece78fd6b5fb0de2f7308ac0fbfd43c439c7aa2565b3f55debe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e20a2d00dc54bf55dbd0ae0ef8ede061b29016bd52d08a7397983aaa47090e`

```dockerfile
```

-	Layers:
	-	`sha256:0d1669a59b42dad0786e45b0fb05d2b319d234cebf886b7631f0b359c9408562`  
		Last Modified: Wed, 27 May 2026 00:11:19 GMT  
		Size: 628.0 KB (628011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a131e4df604b347dfb18df92cdd2b59e78429008b53bc42241fa401a170356c8`  
		Last Modified: Wed, 27 May 2026 00:11:19 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:19554911c47613ae6ca07f99f965ac6d27462850ea0a0cf0bbad1056de98cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23671207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6ba93600f44bddef31b2b7168f991b5055f687153a2ea5dd77891912f28221`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:06:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:06:44 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:06:44 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:09:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:09:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:09:08 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:19 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:19 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb82e239d1cb105364b7d91bc4853a1f789b4f7e41d3782ab292bfd3db0a345`  
		Last Modified: Mon, 11 May 2026 23:09:15 GMT  
		Size: 457.1 KB (457146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b835f0934e73f28d203c3ff75776b2a5a43d86760a57ce7d574e85014044a1ff`  
		Last Modified: Mon, 11 May 2026 23:09:15 GMT  
		Size: 13.4 MB (13364500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a89c556155002cb361e3cf5aa6f10349d85007b6ecaf10c12617dcb8d366370`  
		Last Modified: Mon, 11 May 2026 23:09:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dfcbbb9aa001b46303f91ea7abc184b8f9c2a32359a7658cbc8c1d55e50808`  
		Last Modified: Wed, 27 May 2026 00:11:25 GMT  
		Size: 5.7 MB (5707419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:4683453fcc4e64e8abef7eae5b6cf167f33bed34307eca5ae5cb356df1213a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d3c5145593ae0d67f12300850c22f13a3db2c6e42171b442d1f54c643a11d`

```dockerfile
```

-	Layers:
	-	`sha256:5f6e43793cc434a8b47672bcfce960b0f30a871f1de5250d2315e6978c070c1d`  
		Last Modified: Wed, 27 May 2026 00:11:25 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5feb9e787128a7be6c6d7bd1aa2571ac3a24b2bee0941897ff4aed727545053a`  
		Last Modified: Wed, 27 May 2026 00:11:25 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:6a49a94a24e35aa2aef07f5e1661ffaf208d55afc4e64f60844ee60e94414719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23454732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df2184660820b6ab5a3f2122e22e43d5364110332d181317c846afe366239b3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:11:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:11:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:11:10 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:11:10 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:14:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:14:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:14:09 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:36 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:36 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c753e545eccee86720815518c3770c85ba185e855ce8b8e9880666651aab9cb`  
		Last Modified: Mon, 11 May 2026 23:14:16 GMT  
		Size: 455.3 KB (455266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbbfbe72cef1e36933c1771b7913a5704498e013b78bf39aa22a1e4aaabf77a`  
		Last Modified: Mon, 11 May 2026 23:14:16 GMT  
		Size: 13.7 MB (13667060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead2234c6cb3c187a5b60efbae61cad498a6082dd56832a410c1f812754f1794`  
		Last Modified: Mon, 11 May 2026 23:14:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3259e78b40bb3995a6afab5f3991d22c428129ab4b4bddb54c2b8c4e437415`  
		Last Modified: Wed, 27 May 2026 00:10:42 GMT  
		Size: 5.7 MB (5707434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b2f3aa2e24905cb6139c291c97064ad20b85126c93877632a1bf385c40158993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.1 KB (634140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1acff1092e96ef9aa10deb7f6d4fddbf993acef9e188bcaf0fa965c7db47c4`

```dockerfile
```

-	Layers:
	-	`sha256:e77d72faf1006a9a0c81a90e001e539c05c0d8a9b293398da2c7dfeb6ffd95a8`  
		Last Modified: Wed, 27 May 2026 00:10:42 GMT  
		Size: 624.9 KB (624908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c157c95eb51db123a934e6739112fc6bcb65156c066d1451e41080d397e7e47`  
		Last Modified: Wed, 27 May 2026 00:10:42 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:beb74e147929ec31628c7eb89811cb95cab4be81e49b1ec6cce7a509f6074147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24068633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976fc748c42823fcc4b634ce8ac498f22c41b61262cc5df2c82cb51833b8c5a2`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:06:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:06:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 12 May 2026 00:06:52 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 00:06:52 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 12 May 2026 00:10:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 12 May 2026 00:10:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 12 May 2026 00:10:10 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:20:20 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:20:20 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:20:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:20:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d0b4dafee419db5d6a8b655b46eb0bc8688d9c9e5b1fd869c4611eb9f97c05`  
		Last Modified: Tue, 12 May 2026 00:10:22 GMT  
		Size: 457.6 KB (457587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e56a581d91a21191ab7bf569889eb73e542de4affd9659ef41d622915c047e8`  
		Last Modified: Tue, 12 May 2026 00:10:22 GMT  
		Size: 14.2 MB (14166525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52846d05006358cd35ed2a42c39064adee687201a81d9d6637d467e9a52150a2`  
		Last Modified: Tue, 12 May 2026 00:10:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e40cab3362ef8055f0a06085c68f9a94716f3e8774865aedb24b6b73611b16`  
		Last Modified: Wed, 27 May 2026 00:20:31 GMT  
		Size: 5.7 MB (5707616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:de5ff1bf95515355a0af1129da00af78bb31e868ac5107c3988452505b8ac3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc233c489b440c1927708e41982e4c2e2403beb8397457b8d56906f56a649145`

```dockerfile
```

-	Layers:
	-	`sha256:d82eef0f786026050eaa4088487924c59bc28f934a7e240efe170267039c895f`  
		Last Modified: Wed, 27 May 2026 00:20:31 GMT  
		Size: 623.1 KB (623060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d5e26b2bba0365ad1584135f1c1beee700e555154af0d082bda38c35a8226a`  
		Last Modified: Wed, 27 May 2026 00:20:31 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:0b91e02371a2acf537bfb4ff2f4e327e10a86f57658b20ea24f1bdd0215eac3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23227286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28ff71c5764607565aa910595fa9b5f7318d2099633428c852cbfc4148d1691`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:47:17 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2026 19:47:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 13 May 2026 19:47:17 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 13 May 2026 19:47:17 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 13 May 2026 20:26:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 May 2026 20:26:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 May 2026 20:26:01 GMT
CMD ["python3"]
# Fri, 15 May 2026 13:52:48 GMT
ENV HY_VERSION=1.2.0
# Fri, 15 May 2026 13:52:48 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 15 May 2026 13:52:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 15 May 2026 13:52:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217bf984dca9cefe243681ba1e0ae48ac827915563fbded95cc12508be473287`  
		Last Modified: Wed, 13 May 2026 20:26:50 GMT  
		Size: 455.2 KB (455185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c019ef2c10f8db541191d17296d3bed14c7d6fe51142316e42b45448a025c75`  
		Last Modified: Wed, 13 May 2026 20:26:52 GMT  
		Size: 13.6 MB (13555404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5851b3a439df5a8ca6a81d1e4528c90ac53602e7c500c9c28b28c2e8f2448407`  
		Last Modified: Wed, 13 May 2026 20:26:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fcab552f0926ed8bfb55e1ec90881bc5f9a05e68ffda112b85ae87eaaf56b3`  
		Last Modified: Fri, 15 May 2026 13:53:27 GMT  
		Size: 5.7 MB (5695567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:9abd5b1563ecbea0d2e52669dd82376ae60cdb042ffe5c2d087930a072415f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c575470d20af28c490cd5110efe1095ec3989a277303749ab10ad3a9de6d5`

```dockerfile
```

-	Layers:
	-	`sha256:096e437d4dd26a89e37f31ae0a738d499e633cb2d1cf263987b164b0ab11ae1c`  
		Last Modified: Fri, 15 May 2026 13:53:26 GMT  
		Size: 623.1 KB (623056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79cffc963d1f6c47a29c37831e45d93e996accd197683e2a7ec99c4ce427bfdb`  
		Last Modified: Fri, 15 May 2026 13:53:26 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:d1d6a53fcc92d3245c0e7da6d14b4c7c19698f4a5851d5f87b62802fb5399005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23696591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f186287c5b7a838d0b29d0727273b21fb824b53ee5daee3a82789d65a17fc3a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:14:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:14:04 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:14:04 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:14:04 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:17:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:17:59 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:15:32 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:15:32 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:15:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:15:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c282f76d6267281c96ab3c8e561e5ba01103839b52d9a33a469480d808256`  
		Last Modified: Mon, 11 May 2026 23:18:09 GMT  
		Size: 455.8 KB (455833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8046752018ac9f005ff5bd195779ffecf539029a5b419f81581674c0a15fce05`  
		Last Modified: Mon, 11 May 2026 23:18:09 GMT  
		Size: 13.9 MB (13878952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776e9b721ac7effdfaa80bc4448202ca71a445be656899721f431a88ae6ad37`  
		Last Modified: Mon, 11 May 2026 23:18:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2318c60499d5b0652e9b86532ef054901140c50e5062b4b3ece4b3dd63588b1`  
		Last Modified: Wed, 27 May 2026 00:15:46 GMT  
		Size: 5.7 MB (5707684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d279e7bd50a4a390ad763a709b040e07551d9343af0403574e713f9aa6ba6b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f60fb72baccbbe6d195bd19d6cc498882d27846f9e4cbb92619137649eb7d1`

```dockerfile
```

-	Layers:
	-	`sha256:b7be0257b40d1befdf40e256fe3caeb65eb5b539402b5bbfffaef7f0f79cd2ed`  
		Last Modified: Wed, 27 May 2026 00:15:46 GMT  
		Size: 623.0 KB (623002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458c10be50ecb3ade0efc651df6cef0ee7f76aa108d032870d38d56a79d6226b`  
		Last Modified: Wed, 27 May 2026 00:15:46 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
