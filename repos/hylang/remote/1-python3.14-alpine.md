## `hylang:1-python3.14-alpine`

```console
$ docker pull hylang@sha256:d54bef66f5d759126e454848fe09b4cd35dc7be33b7bccef75dc8ee4ac2726e0
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

### `hylang:1-python3.14-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:49b88816964d2291288dc4d3a45d5e3e57b313577a0d82a7c912f2568f496ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23294892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc9074ab3109e80e120bd1d2e60a4e90ecbcc12bfe776065fc9c09302611562`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:46:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:46:59 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 20:46:59 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 20:49:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:49:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:49:28 GMT
CMD ["python3"]
# Wed, 15 Apr 2026 22:08:47 GMT
ENV HY_VERSION=1.2.0
# Wed, 15 Apr 2026 22:08:47 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 15 Apr 2026 22:08:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 15 Apr 2026 22:08:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5404ec0dd73e7f052f8c5ba25a6b5a74648c6cf447615b30026da2e7feed046c`  
		Last Modified: Wed, 15 Apr 2026 20:49:40 GMT  
		Size: 455.7 KB (455657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb975258b557670c54a75dcef1382e512b3e25d7fe4107242ddf1b93a0b0df51`  
		Last Modified: Wed, 15 Apr 2026 20:49:41 GMT  
		Size: 13.4 MB (13394216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067ea42d32c497ea1600b9297c31c1ea49aee050da96837b8510a2dba63cb69`  
		Last Modified: Wed, 15 Apr 2026 20:49:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea062d543b8c2b42f1d6a2cd6f5f03fbc5fd77c32dd0289614d3749fd5fba4`  
		Last Modified: Wed, 15 Apr 2026 22:08:54 GMT  
		Size: 5.6 MB (5580582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:9f2c2184b705349d90fbb546b0f349f55db1ff4c91132d641498bd0ebff94375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ce396fd2fe78a5463d3b59aa0053115aa3ecd21df7ce3f3c11fa59a05f040b`

```dockerfile
```

-	Layers:
	-	`sha256:f81a8f94681b042b05fb6fa2301abde23dc54990a2884c95cad75665fd362cdf`  
		Last Modified: Wed, 15 Apr 2026 22:08:54 GMT  
		Size: 626.2 KB (626200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87aad124f124797257f308d657881883c443c891bdc218aaf18da96002f612d1`  
		Last Modified: Wed, 15 Apr 2026 22:08:54 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:1e3ab1aad3da669cd170d86221adb7e9838db86ef83cee88a1e41afad7737863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22630291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21c7d1aa1aec4354128388cb2b5e94edd17217ad7ae80a987385e6260d0195d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 20:32:25 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 20:35:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:35:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:35:14 GMT
CMD ["python3"]
# Wed, 15 Apr 2026 21:26:32 GMT
ENV HY_VERSION=1.2.0
# Wed, 15 Apr 2026 21:26:32 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 15 Apr 2026 21:26:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 15 Apr 2026 21:26:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cf22b8a74dcc332c9d0aee3f6fdbcfba5b8b917dc57964b1b8c0a68fa74ab4`  
		Last Modified: Wed, 15 Apr 2026 20:35:19 GMT  
		Size: 456.5 KB (456518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b71d8e95ceae535a647ec9803f7dfb63519da459b02d7831fc424c99a05bcc`  
		Last Modified: Wed, 15 Apr 2026 20:35:19 GMT  
		Size: 13.0 MB (13021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e891f0592292904072cd0154346781d2cd8bb43893319318999505524cbd019`  
		Last Modified: Wed, 15 Apr 2026 20:35:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be40cb28abdbb24a055c48cc994ae5ae358c7327e49cad82b95392f16524c6d2`  
		Last Modified: Wed, 15 Apr 2026 21:26:37 GMT  
		Size: 5.6 MB (5580518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:9cc7c1272e5959915f8ec187f33c7511e5e33027080ccda058dd3ff82c0ce3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 KB (11765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee154dbaa6bbc7fdebc2730c75ae3046c75b1617195180b82f9f0b68fc224c6`

```dockerfile
```

-	Layers:
	-	`sha256:8ce1dfb19e07cb662b23c92b9c8ea9f47afed01edce602e1222f40a7552cbbe1`  
		Last Modified: Wed, 15 Apr 2026 21:26:36 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b25cbc96539d78e7352d8375bb3c9ac9631dd815c33b99f3f89cca95900de278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21943598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1cfc33570d4f2193d30b78bf3f4ebc0b97703ca90e44760eccda94471a9cfb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:42:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:42:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:42:22 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 20:42:22 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 20:45:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:45:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:45:08 GMT
CMD ["python3"]
# Wed, 15 Apr 2026 21:40:54 GMT
ENV HY_VERSION=1.2.0
# Wed, 15 Apr 2026 21:40:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 15 Apr 2026 21:40:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 15 Apr 2026 21:40:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0589cc5664c777bd5991794aae3771728371dd697b2e0f14bba9e3dc3ef83caa`  
		Last Modified: Wed, 15 Apr 2026 20:45:14 GMT  
		Size: 455.6 KB (455633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997fe038125e703d76ae7021dc0ce94b9ce13a9d47857d2eaa4dec1975dbec2f`  
		Last Modified: Wed, 15 Apr 2026 20:45:15 GMT  
		Size: 12.6 MB (12623984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd447a0a7b6828c47236e059f6b0698ad652725976f14ee195bb1891ae183772`  
		Last Modified: Wed, 15 Apr 2026 20:45:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab43257d18cef7ed46737c666f2da069f0b83711e77f4745f37d98ac0f1764`  
		Last Modified: Wed, 15 Apr 2026 21:41:00 GMT  
		Size: 5.6 MB (5580609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:9cd3ff58dbd7fe875ef903ba4b19054dea1233cf89e31d2aacf96b6a3776abbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f953a8750fa2f638092dc7c338059780a8cc5b2579e6f98c506e591373400`

```dockerfile
```

-	Layers:
	-	`sha256:6315ef1c5c1b7504c4dd2e13747f27c175c531549dfd57dc50ad0e198e541964`  
		Last Modified: Wed, 15 Apr 2026 21:41:00 GMT  
		Size: 628.7 KB (628672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cb82505766e4dd3fab0a3255b93cd9b1c33d29a1d66155fcfbb8384e0ab31`  
		Last Modified: Wed, 15 Apr 2026 21:41:00 GMT  
		Size: 12.0 KB (11979 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a4330813a94ca2ba94bf692bc69499a7a6d4aa61a869893d313d9d99b3adf8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23721451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ebe3aca40b4959276a10de7c7dfd754512a1b6a1b4cf6b313892e3db7d4b9c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:47:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:47:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:47:05 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 20:47:05 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 20:49:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:49:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:49:53 GMT
CMD ["python3"]
# Wed, 15 Apr 2026 22:20:18 GMT
ENV HY_VERSION=1.2.0
# Wed, 15 Apr 2026 22:20:18 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 15 Apr 2026 22:20:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 15 Apr 2026 22:20:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce044e508c31b550012103ac403762a3f10a13a30aa1a69e117060b0d6d43a9d`  
		Last Modified: Wed, 15 Apr 2026 20:50:00 GMT  
		Size: 457.9 KB (457909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9def3ce2dae125b2efcb5100bde3ecee4d9b5f78b9088098753338af9e277661`  
		Last Modified: Wed, 15 Apr 2026 20:50:01 GMT  
		Size: 13.5 MB (13482813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9363636621cd74af602f2571bc4ee6ffe761c3ddcdbb85e4e29d3044e1d555e6`  
		Last Modified: Wed, 15 Apr 2026 20:50:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1362c63f7cad706ee0ece7282fbf2d9ac1842652bcd4b27d0a40fc6dece52787`  
		Last Modified: Wed, 15 Apr 2026 22:20:24 GMT  
		Size: 5.6 MB (5580609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:3d9eefbad7ade3b4c9ee4fc7a6a8e63b3db2aa638d86c89b5b7e4a9fbc134d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cfec460746d2ad7690e8d91b86790493dc4fdaefac2d9e22479d1255079719`

```dockerfile
```

-	Layers:
	-	`sha256:84b653ab0879893848b7bbe0d74524dc960da6d1c2ceb9288bc81578f3c12f63`  
		Last Modified: Wed, 15 Apr 2026 22:20:24 GMT  
		Size: 625.8 KB (625750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052951c69f392b2fb3d41c53adbe056c6690ac1a7e43f3ed7d96b2119ae37db4`  
		Last Modified: Wed, 15 Apr 2026 22:20:24 GMT  
		Size: 12.1 KB (12051 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; 386

```console
$ docker pull hylang@sha256:c34ceb9821b769992b665814e1e291df449db7f92056c97198ad52b89c11c10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23379412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902bcc832a46d05dba09cab60402f9e3895c3731d3ec6e1afeacf711f7ab5e37`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:27:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:27:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:27:44 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 22:27:44 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 22:30:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:30:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:30:32 GMT
CMD ["python3"]
# Wed, 15 Apr 2026 23:20:22 GMT
ENV HY_VERSION=1.2.0
# Wed, 15 Apr 2026 23:20:22 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 15 Apr 2026 23:20:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 15 Apr 2026 23:20:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af3df38f7676f55ab3f69e45ac65f764505665e1acf2e2756dcee5c754cc728`  
		Last Modified: Wed, 15 Apr 2026 22:30:38 GMT  
		Size: 456.1 KB (456107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b86cb474141324098f3baf3babf3971d035cacd2a61920c252d521be38dda7`  
		Last Modified: Wed, 15 Apr 2026 22:30:39 GMT  
		Size: 13.7 MB (13652097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ce068292bb245f7f9322d68f99b8bc7c333f907a3cc1df3229ff3d3eb044`  
		Last Modified: Wed, 15 Apr 2026 22:30:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6de14f798f41366411f04f4d8f2fa6affc2274b829fbffcb0aa3a989907fd`  
		Last Modified: Wed, 15 Apr 2026 23:20:28 GMT  
		Size: 5.6 MB (5580515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:5dca5382dc63a070530a4b2305c2a74437626e66803971808c79ada8bc7c0651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f78a2a7ae8fcd15f75a54ab30b949ada64af5795dd29a55654ff2ea6da84d4`

```dockerfile
```

-	Layers:
	-	`sha256:5b6b7c06ddc46a406c9216131fb844b0a948ee0022d1c621011acd3c00e81a75`  
		Last Modified: Wed, 15 Apr 2026 23:20:27 GMT  
		Size: 626.1 KB (626115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e2ec135bd4f40c9b50532191345a65c204f9d2018f3b172b36fb0a01b09861`  
		Last Modified: Wed, 15 Apr 2026 23:20:27 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:caed249ffe37c3745b15b7199a55a18b2bf1d792ce248e4a0420c8e787d55914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24143846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233f1092998ca78e12d241f049c2c9ecee559deff9605955dd145937855659fc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:24:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 22:24:53 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 22:28:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:28:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:28:54 GMT
CMD ["python3"]
# Thu, 16 Apr 2026 03:21:37 GMT
ENV HY_VERSION=1.2.0
# Thu, 16 Apr 2026 03:21:37 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 16 Apr 2026 03:21:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 16 Apr 2026 03:21:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733c1cad5f8e0c40c970a427f687a14dcfa498e80380cc189bb3aaa48c76c673`  
		Last Modified: Wed, 15 Apr 2026 22:29:06 GMT  
		Size: 458.3 KB (458317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6602bd68768ba979ff14e736312a849c3ad4bd7db0a309bc0f4e237bcb3a2fec`  
		Last Modified: Wed, 15 Apr 2026 22:29:06 GMT  
		Size: 14.3 MB (14273720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3705ebc6267a326702fa90841e1e0fab8ef771157866adc791a64f550430790e`  
		Last Modified: Wed, 15 Apr 2026 22:29:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93c81be46d248ce30852074f6a1050f0adc4044eb850df7b9f0e2a17d14e41d`  
		Last Modified: Thu, 16 Apr 2026 03:21:49 GMT  
		Size: 5.6 MB (5580632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:d9ec102eacdda146d0457dac60bea256b1bc43c1e07551d6abf2651ed27da681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce7921d073df0d5535a5ebe0d7aef6f274953a6e36bc1c3a020a52804123039`

```dockerfile
```

-	Layers:
	-	`sha256:04c4eaa93cee5e651087b83714b3bd7a1a3eabdfc47f65fe4b9168f12b0a1bb4`  
		Last Modified: Thu, 16 Apr 2026 03:21:48 GMT  
		Size: 625.7 KB (625655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf94c07d0ccb1aa0e05fead7f7cf75fd24fc01d0b485067b3ce6707f76f254a`  
		Last Modified: Thu, 16 Apr 2026 03:21:48 GMT  
		Size: 11.9 KB (11920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:18ee0ec3025f78e4a0ebf9df044febd75b6b191fe59967d0c2e18877214e4ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25883155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfbdf043a798e9abd877a2a890db27069da32f1ab8bcfa7d5c59bffc6cf7ff6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Apr 2026 12:45:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 12:45:18 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 11 Apr 2026 12:45:18 GMT
ENV PYTHON_VERSION=3.14.4
# Sat, 11 Apr 2026 12:45:18 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Sat, 11 Apr 2026 16:25:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sat, 11 Apr 2026 16:25:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 11 Apr 2026 16:25:02 GMT
CMD ["python3"]
# Sun, 12 Apr 2026 19:29:59 GMT
ENV HY_VERSION=1.2.0
# Sun, 12 Apr 2026 19:29:59 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 12 Apr 2026 19:29:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 12 Apr 2026 19:29:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8e519c1c891161f6b43ccc690b8e6539209e3308919938993e61bc095ff00`  
		Last Modified: Sat, 11 Apr 2026 13:27:25 GMT  
		Size: 461.0 KB (460994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b86b1ac44889d350209911f02cb8e24cbaa97db4e1d4294932acd42934e471`  
		Last Modified: Sat, 11 Apr 2026 16:25:53 GMT  
		Size: 16.3 MB (16274367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f66ef2f3c34ba4fc9f7c28fb4d25c7584ad76fcb4de1951534cc93471e426eb`  
		Last Modified: Sat, 11 Apr 2026 16:25:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad6f69a324930e3f549fc9164f5d75e6963d04c8a44b5b0fc173c7e46f20367`  
		Last Modified: Sun, 12 Apr 2026 19:30:37 GMT  
		Size: 5.6 MB (5562257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:1a7ae7e5df25438d6920293081b362f686af421065ca17c8c499bb1d70aa45d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee65fad664971e178e5fd9784580e7d5dfc67e34fea3111cdaade04299ca7`

```dockerfile
```

-	Layers:
	-	`sha256:892a0d35d4d34a5b418903408cec7781f5340364e36d5128e10a5f48d7cd8c69`  
		Last Modified: Sun, 12 Apr 2026 19:30:37 GMT  
		Size: 628.6 KB (628629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc8719d932f95b3f2d42808ab367b6e11ace2947c4e7546ecc216d32c3fe06e`  
		Last Modified: Sun, 12 Apr 2026 19:30:37 GMT  
		Size: 11.9 KB (11920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:e2a105bb8b1e2c0e82fdde9a2024dfa2ac18822388edf98c6787ba0db2a6d7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23641202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042b45a877d5679e2b017a612d09f583c57f7e77cfe7973ac452b8635a27987c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:17:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:17:53 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 15 Apr 2026 22:17:53 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 15 Apr 2026 22:36:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:36:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:36:46 GMT
CMD ["python3"]
# Thu, 16 Apr 2026 00:48:17 GMT
ENV HY_VERSION=1.2.0
# Thu, 16 Apr 2026 00:48:17 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 16 Apr 2026 00:48:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 16 Apr 2026 00:48:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d783dc3f612930ddb20e808297a0ce017500fb3f8134bae566eb50ec93746`  
		Last Modified: Wed, 15 Apr 2026 22:27:13 GMT  
		Size: 456.7 KB (456670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05d68580a9d50029bb9cef947da00e9e24ac7109d16f64c3a8eeb04061f8e1`  
		Last Modified: Wed, 15 Apr 2026 22:37:22 GMT  
		Size: 13.9 MB (13877382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08885db1de77ddc523201775a1218bab73fd4d406980ccc664ec08e5f6889779`  
		Last Modified: Wed, 15 Apr 2026 22:37:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23672c2d0bbbde815f3277613d6bf32550349a1c5842c3678030c9153cefa7`  
		Last Modified: Thu, 16 Apr 2026 00:48:28 GMT  
		Size: 5.6 MB (5580371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:1f83b34b26ccfd716ef5598b7b7b05a0be45465e73db951e8a880a4227116164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25968c5f39ee59c49186b094efd441d635cd12b11be8d473d075d49c77b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:83e58d9aef7dc4b56bde88f9a4ea0cb435599d4426a9b0637ca47bfe327b7863`  
		Last Modified: Thu, 16 Apr 2026 00:48:28 GMT  
		Size: 625.5 KB (625549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd115a9c11fcb64d344b7b0f2a6d483da4db2061170c3d774304168fcfd4ddcf`  
		Last Modified: Thu, 16 Apr 2026 00:48:28 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json
