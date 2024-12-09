## `python:alpine3.21`

```console
$ docker pull python@sha256:736458a5572d7e3df200a4b6ffa245393e2d5e89c68cf0d5b83730920d6ef1d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; 386
	-	unknown; unknown

### `python:alpine3.21` - linux; 386

```console
$ docker pull python@sha256:3a98017e1188a4b3067cbfeedd6a9c39204cf2c6908d1fbc90acaad2896138cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16665785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42af4801e00973e77729aff1c55468b68e19e4d4d2fee1ec264c4238ebddcce7`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f84b7ed00674bc6406362a3dbf1d0054e2e252acccaf206f91a49f205bdaded`  
		Last Modified: Mon, 09 Dec 2024 20:48:41 GMT  
		Size: 462.3 KB (462315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a0b7e9a71424c030c5ca54d5c5ff9c1530b602987a8f7ac416284cb3d3aa6b`  
		Last Modified: Mon, 09 Dec 2024 20:48:41 GMT  
		Size: 12.7 MB (12737140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db913a7ea049c16d9ca613e3f530aa8be294c79939147a651a863b09d5671`  
		Last Modified: Mon, 09 Dec 2024 20:48:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.21` - unknown; unknown

```console
$ docker pull python@sha256:68b0469586d101ac483ebd3c714d8a11f4270c138df310a20238c6429a4aafa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.2 KB (645151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e64305c886dc2945d8db7697140b2ec09508854e6b779e983a95e18bdad5b3`

```dockerfile
```

-	Layers:
	-	`sha256:d08570ac35992f4ea61de25c8254a103c1895bfb1ceb1d9c201fada54a60b9ed`  
		Last Modified: Mon, 09 Dec 2024 20:48:41 GMT  
		Size: 623.5 KB (623490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4941374d11e0c37211eb89034e17c143ec2d0b5fc1854a0634a85de14b545c59`  
		Last Modified: Mon, 09 Dec 2024 20:48:41 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json
