## `hylang:python3.14-alpine3.22`

```console
$ docker pull hylang@sha256:01de0dad40491909763d152ce3c03dfda237742ac8e43a1107887c128572c6f5
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
$ docker pull hylang@sha256:0e0ad6cf55f52aa991b743aa476430d9b3e5c3f5855e701ed7a1ac0c73fbc892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb58ac38e0b72727595dbca42ec689c839b5fcd4d4a3bbb288ff60c054332ea2`
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
# Mon, 08 Jun 2026 22:44:44 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:44 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:44 GMT
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
	-	`sha256:3aea7d2fa84657497b4616133ddb2736b29ad76207e24a233710eb2034c69dd1`  
		Last Modified: Mon, 08 Jun 2026 22:44:50 GMT  
		Size: 5.7 MB (5711700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b10af3fcbb5bf5241e3e44e2f76dfc141cd8337054170640eaff17146dd1d74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa110e6954edc6f6da190c3af84f9a129b6cddc457e6aaa97df6ee867859e82e`

```dockerfile
```

-	Layers:
	-	`sha256:f8eb0fa141eb3aade94291a4b31441a57171320a64670a833a0c7001fc7f565e`  
		Last Modified: Mon, 08 Jun 2026 22:44:49 GMT  
		Size: 625.0 KB (624953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf9bf2dd8c40ca061d5f665d341a717eb5d1ba166cb35372fb742f2f73942d8`  
		Last Modified: Mon, 08 Jun 2026 22:44:49 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:4d5b1bad46fac49effaf69e0993ab5307000d81823e5850d6354e555f5fb9bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22650858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc4fc65031b2fdab7d7cd2f9291fe2e83d64c583c27c619a5412bbb17c29f5e`
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
# Mon, 08 Jun 2026 22:44:21 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:21 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:21 GMT
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
	-	`sha256:16ddd616e36d3b6648597e43ce9e699d25532bbe9dc3689397407253ee71fdab`  
		Last Modified: Mon, 08 Jun 2026 22:44:26 GMT  
		Size: 5.7 MB (5711779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ee9d13967f5f194ecd081bbd40102d55dbc457b56b44b453c9c837077694fb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2637d8ea3a1d42bab9607c2cfa4519f5e8ff9ec1d21624075d10e79591659c`

```dockerfile
```

-	Layers:
	-	`sha256:097d468caaa490eeb8625a6f6822ee1dacb2d654b515154d9517e9033f5164fb`  
		Last Modified: Mon, 08 Jun 2026 22:44:25 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c8fe683c30009b6808669f485a3a6e3747053b6853bafd41af2a5913b22cd9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21985428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddf06cf68b47e6cae22277603cca0d19f479e74aae619bcd2ea5e5d090175ed`
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
# Mon, 08 Jun 2026 22:46:26 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:26 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:26 GMT
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
	-	`sha256:965c4045e37af608d5c7e4143791b028f77744182b2c792c0b9ea87394a370a8`  
		Last Modified: Mon, 08 Jun 2026 22:46:32 GMT  
		Size: 5.7 MB (5711690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:7002f9fbca48ebdb6c7f1a8c8d0450262df09ad50d7e4730ac04be1edf2f7dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b27e0755e1ebf494d627b95218c6808b431c86d7a85364b39bfece99d472c40`

```dockerfile
```

-	Layers:
	-	`sha256:76c89f7e836295e16bb5df9951b2352cafd6dfd38beb21b5b1d7d24e4ac57c82`  
		Last Modified: Mon, 08 Jun 2026 22:46:32 GMT  
		Size: 628.0 KB (628011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82331b501aa713527886ff6f19c3dfb77b2e88ec936665cfda253fe13d1c88bf`  
		Last Modified: Mon, 08 Jun 2026 22:46:32 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e5aa513dcba6f92792343e4e038463676e4204910e0ffefaca960c18ec684d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23675491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab5f2e50d7d9e77d78af721b8ab0d3d8c985f28ea1d451762367113fc2f7c1`
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
# Mon, 08 Jun 2026 22:44:51 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:51 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:51 GMT
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
	-	`sha256:6da524a8ccb5c1fa39e64c035e48df52dac19d00e57883614182b8e3bc0cd462`  
		Last Modified: Mon, 08 Jun 2026 22:44:57 GMT  
		Size: 5.7 MB (5711703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:f4d94257f355535fd5e8602dd2b0732526b92c8f72213ec3900261179aad7f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182ae9bbdb48841d6b3e99da1f3a0df6ab201edde07890f6ba8cad64b89c9755`

```dockerfile
```

-	Layers:
	-	`sha256:21ff18e27281a1ea29f042ca571cd659c7eca67e6ffed2e01a44c2411ad3d608`  
		Last Modified: Mon, 08 Jun 2026 22:44:57 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca95f2dbcf56da177948db0285369467b3d5cf53a904da43c6c4b4dda0062c3`  
		Last Modified: Mon, 08 Jun 2026 22:44:57 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:47a51fcc0dcdf0e9d84d13533b9ee6cfde3f228d01d650ebfa5427bb4f2f0451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23459005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aa8ace6499706ce4f6a1731fa1ab131c4cdaa7a2ad004a739c5593e8b1e0bb`
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
# Mon, 08 Jun 2026 22:46:37 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:37 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:37 GMT
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
	-	`sha256:a0390cb684930b85fbe9dd0be62fd936fb9df02420d83c88c1da402fd247076b`  
		Last Modified: Mon, 08 Jun 2026 22:46:43 GMT  
		Size: 5.7 MB (5711707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:74543bbfe8d6a2e4a7572d3c634c96bd6eae9a89c28085b0c9c6f381ffc8ee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.1 KB (634140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c1839052bb15e452414cb4022deb09bab383676f0a7b2b867406eb3e1d98ae`

```dockerfile
```

-	Layers:
	-	`sha256:136a4a6be2eda3c0028baf2d528ef2b7f36af1f8235921f19001bb826e2a269c`  
		Last Modified: Mon, 08 Jun 2026 22:46:43 GMT  
		Size: 624.9 KB (624908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dfd421a4528ecd9e835c83881fe83e7ce318f7834ca6f916688722a2857b430`  
		Last Modified: Mon, 08 Jun 2026 22:46:43 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:8d54eef63aea7ad6024ac2a7b63ada844ea27c85831fd259dcb76866009dba97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24072872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5e27fc98e3f8af60963dae310df55e1c3c4019e0ba173aadc4de753d0929d2`
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
# Mon, 08 Jun 2026 23:16:04 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:16:04 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:16:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:16:04 GMT
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
	-	`sha256:3eab8f21cf319a56d7c87f6cfb9441723f1ac48fe573b09234969d335e9765ca`  
		Last Modified: Mon, 08 Jun 2026 23:16:15 GMT  
		Size: 5.7 MB (5711855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:840e0187b2a9745f1b14412700cc9f03a440024c86587b46fb6e9e97e34ecb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cb68a215ae8d31c5901831c99cda0d49a0eb5e94647d9d2286ae0ac5833d0c`

```dockerfile
```

-	Layers:
	-	`sha256:2a731e33783f09c99023932248127b482003020e187f164df99640647dfb2be6`  
		Last Modified: Mon, 08 Jun 2026 23:16:15 GMT  
		Size: 623.1 KB (623060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa876929e40df986e3a90fd36a64bbfae66932c151663ce0a81960cf9f5df8e8`  
		Last Modified: Mon, 08 Jun 2026 23:16:14 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:c2cbc89836d4aab1dd8c87d6b372014f3e81a9bb9c9903b849b18810f8b22592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23240121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52d4144a395c7c82d55da46e51f007fb48e405fb9d94912ec3fef3c68ba8a56`
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
# Thu, 28 May 2026 12:06:42 GMT
ENV HY_VERSION=1.3.0
# Thu, 28 May 2026 12:06:42 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 28 May 2026 12:06:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 28 May 2026 12:06:42 GMT
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
	-	`sha256:16cad2d0da636d128c4782be36dad0a80d841550c109332fd4efb67f02886093`  
		Last Modified: Thu, 28 May 2026 12:07:22 GMT  
		Size: 5.7 MB (5708402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:cb4607af038deb5f7bce38d0d010c963e44240a8213c63335db188e5731cdd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09391d53c37d25ccf94a1c39bcb8d8c8332ff90fb00801d3ee0a0b62559d7232`

```dockerfile
```

-	Layers:
	-	`sha256:2ae9f016f6208de95827d27a57a040b94ffdfe5830e1af5d4c1fc3224658649d`  
		Last Modified: Thu, 28 May 2026 12:07:21 GMT  
		Size: 623.1 KB (623056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b125222b2dfe297006c996886b428040a6e9248d0f6b5f3754044dbf2209175`  
		Last Modified: Thu, 28 May 2026 12:07:21 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:3baf14cbcb8b68b55b1373562bb481351b1b388dc94a786bce75be0780e7a76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23700612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875542202c3bd2e700bbd84e0d436e576f8a7802b7d01200c1f560f5e491a70f`
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
# Mon, 08 Jun 2026 22:54:40 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:54:40 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:54:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:54:40 GMT
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
	-	`sha256:97e76627212948bc4794ab229c3d46999375b1a705b448897b76b4fe83882a24`  
		Last Modified: Mon, 08 Jun 2026 22:54:51 GMT  
		Size: 5.7 MB (5711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:57b63b08cec327d40fce2e2cd20a275bbe6986ee15d0a2b00540ac30d43d0a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3f2d936dadf380018a694bd11fa308b04faf763cf09ac5aa63cac5b24f91f0`

```dockerfile
```

-	Layers:
	-	`sha256:edc911b1d063cfbde05494d73cbb5d93824bf1509cd28e1f1b4620a90fa99758`  
		Last Modified: Mon, 08 Jun 2026 22:54:51 GMT  
		Size: 623.0 KB (623002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63cc2d913227198882883574b423e91927b07e40fd8a8fd9110ffcc033bab20`  
		Last Modified: Mon, 08 Jun 2026 22:54:51 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
