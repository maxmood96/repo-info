## `hylang:1-python3.11-alpine3.19`

```console
$ docker pull hylang@sha256:e947eee88a59cb3fd637f5dc7d5fa67bc2cd2a0d760832e42f2687aa8e59f44b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	unknown; unknown

### `hylang:1-python3.11-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:07fe9af34001f96d2a9a154044ef7e5b57dae8c007c8a88a5b33347ada834866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25433186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae74027cd54d6cebaea013c43ca637ccda96a33c45c693d74175d3c6bf08c59f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.11.10
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a39bdf9d326d55be66a6472913d0bdbe3b64af11a3fa17f368b4581b594e62`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 628.8 KB (628820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d733b3ae7d98d7ffaec734f38430ab78a0e5d925a1dad723829fc970fd94483`  
		Last Modified: Thu, 12 Sep 2024 22:44:01 GMT  
		Size: 15.4 MB (15409477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a382324fda32eee9487659d9575da68c88bdc216cf9960b4e77a0f097bd81742`  
		Last Modified: Thu, 12 Sep 2024 22:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3316c736ebdb8ee14ae4ac25aaa2e1f10a61f286e894387a1b486031b7c1e7`  
		Last Modified: Tue, 24 Sep 2024 01:19:02 GMT  
		Size: 6.2 MB (6218250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:c22edb4285cf7954a80815e9fcd34e6871ac3887b9afca2a5aa212fa79957807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c238a6b420f92e2b558f1b86c2d481cd04899cc2fc5384e74a8ef90f06bd98`

```dockerfile
```

-	Layers:
	-	`sha256:834e2923886f218b748899c958f01d9a2e73b9c98a0e029d479f691316176c7c`  
		Last Modified: Tue, 24 Sep 2024 01:19:01 GMT  
		Size: 7.8 KB (7792 bytes)  
		MIME: application/vnd.in-toto+json
