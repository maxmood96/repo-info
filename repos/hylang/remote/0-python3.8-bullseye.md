## `hylang:0-python3.8-bullseye`

```console
$ docker pull hylang@sha256:fcaa3ee74c8ddc41a27283003bbb0887b5c3163bf6615ca26e93617eb10f2e9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:0-python3.8-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:a571cb595360424164b3dc901f5ed3677c3cebd2d55b09843a20abe9f2ba98c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49858071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90830a9c4cab84e0819d6486294f07a5fce90ef759d4733a5932c6106c3b400f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a736fc9bbeea3e36926de9b7f4e8e26361993446236d551bd8e0c2674818b611`  
		Last Modified: Wed, 10 Jul 2024 19:12:13 GMT  
		Size: 1.1 MB (1076298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a988442fd2a99509bb0a5d4cb053c16b97f5f3bee0ae0819ba75f2e94a10d2b`  
		Last Modified: Wed, 10 Jul 2024 19:12:14 GMT  
		Size: 10.8 MB (10829065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68352cfc246874906e04c2b33e71c9eaee80f96986e3cfbed26ee3b26f926747`  
		Last Modified: Wed, 10 Jul 2024 19:12:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009242a1af0576ff37a001abc98d0d120ca87591fc16e937c77b45fc3f3d521a`  
		Last Modified: Wed, 10 Jul 2024 19:12:13 GMT  
		Size: 2.8 MB (2773947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd342e63e27ed33d6b97fa7a52b7a7896982707c37b2ec1c214eb1528cd5d83`  
		Last Modified: Thu, 11 Jul 2024 16:58:23 GMT  
		Size: 3.8 MB (3756244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a4685463c9e383ecb555cd751a83b6bd6b732b5066bfcafc1ac4dbc116426773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d9d027120c582a6230852bf7eda7c10b32abd3ff594e57096698950b56e9ef`

```dockerfile
```

-	Layers:
	-	`sha256:43f8f1deb1d7d61087b5e89170642774fb05759d03d29e823319c94f09ddd1be`  
		Last Modified: Thu, 11 Jul 2024 16:58:22 GMT  
		Size: 2.7 MB (2688464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35499b85c3d3b315a53d47887e748e291e79ddfee6adbb6d2d7e481c64d24f70`  
		Last Modified: Thu, 11 Jul 2024 16:58:22 GMT  
		Size: 8.5 KB (8490 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:4c9a05ece4b964fcb5ba403cdd2f82b7eb042f983e912f178d1bcbaf7343912d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47127877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef902485c06c3cb3c7bc419968ffa51959f8cb8c981510628a8b3cf08f829e08`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:43 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Tue, 02 Jul 2024 00:48:44 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:63678471745dce46512f823fc94716da7f08aa84c931dde61ae18c67b55c3085`  
		Last Modified: Tue, 02 Jul 2024 00:52:13 GMT  
		Size: 28.9 MB (28924714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa6fda52fd675c3296bcf24471cef5884c7268e1eed9e5d5a1f42f290c8dbf`  
		Last Modified: Tue, 02 Jul 2024 20:55:42 GMT  
		Size: 1.1 MB (1059710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de83cd9c36fa57fdebc4e378f8389b9e8e11259b2119aeb0ece3483659046f8`  
		Last Modified: Tue, 02 Jul 2024 23:14:36 GMT  
		Size: 10.6 MB (10613109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16003a4a910f461ef2b3049d0b6b8ac0980849d672bd645b89692b22e9584a7`  
		Last Modified: Tue, 02 Jul 2024 23:14:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3036f05ee5f1d3b16b6850fe986b0ccd12d58506aa2a4962631897224222fe72`  
		Last Modified: Wed, 10 Jul 2024 19:22:30 GMT  
		Size: 2.8 MB (2773677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b440799f0fb3ca26f92b79134d32d2ce1faacc962a70cadb490e5b998100dbac`  
		Last Modified: Wed, 10 Jul 2024 20:01:53 GMT  
		Size: 3.8 MB (3756436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3c156b715aacbb8abebadd17ebb648e7e222f706c83364078b199a98977a1f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7d5ca9e4ef13d94e69e594aea71988da9b561cbef3ba8ecd5d7b1aa5749a9f`

```dockerfile
```

-	Layers:
	-	`sha256:ef52fa6a5fd62ed33716bb5755cbad5c5b0aa4c534b5ca9993df67939dc8ba56`  
		Last Modified: Thu, 11 Jul 2024 17:01:11 GMT  
		Size: 2.7 MB (2688706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424c4f44b2c501d11c20519c5c7f3edec777539d0867ea851c20222413c167f2`  
		Last Modified: Thu, 11 Jul 2024 17:01:10 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:9a6b618df4441e8703673e98af55e2e633fd8cdc45a45d466df5d223e13ad2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44359800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144782d0a4ee041ead6d6da80967a238464092fbb3f8006589664b27443996f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d1b8374477deda088db2b2784d203ec3d046360becceaedc483315dda4ef49`  
		Last Modified: Tue, 02 Jul 2024 22:21:03 GMT  
		Size: 1.0 MB (1041728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cad2c1afd09093868e60c3d866615212d55e24ee3966a69bbaeb069ce5fe6d`  
		Last Modified: Wed, 03 Jul 2024 08:48:37 GMT  
		Size: 10.2 MB (10204998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739ef001bfe2761f05f49f7b35e6e5b3dd9876181f0e08ed34b7d63c349b4dc2`  
		Last Modified: Wed, 03 Jul 2024 08:48:37 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f27088bd15eeca9f8804b2a1cdd548ac0bc6c09d5b999a45058d2b16a8295`  
		Last Modified: Wed, 10 Jul 2024 19:26:42 GMT  
		Size: 2.8 MB (2773726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c92a1be8e06d11b78effef4ec213717516e446d83d9ddebba8e76431e1e3f3`  
		Last Modified: Wed, 10 Jul 2024 20:15:47 GMT  
		Size: 3.8 MB (3756411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f6082543be4a6ef392f4da2d92f7ded438acc441fdaa875b2805c68bcecd30ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f68c9fe72d1c88e72edfd01c5197fc5135a32fa1c81a333e0b4be0c2571fd2c`

```dockerfile
```

-	Layers:
	-	`sha256:e5def2949e046fc2ac153beaf15fc16f134362e610a30241ac2eea8ff5f60aca`  
		Last Modified: Thu, 11 Jul 2024 17:03:34 GMT  
		Size: 2.7 MB (2690714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f9087d48f2b5853697d85d86ba6665996c786a3cdfe46ebc71820a54d19231`  
		Last Modified: Thu, 11 Jul 2024 17:03:34 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:52f91ee21d26ab4c0defda8f6103baab0debf74a08cf8d7ff621baee14656e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48584259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ce627ee38602330e253bdcf68c8cee06511b9b21d363893d78d29ea24b1b99`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2197229b63cd075b53e5db849039a3900a119a8b056fbc92b7c606dbf3ecc530`  
		Last Modified: Tue, 02 Jul 2024 21:20:28 GMT  
		Size: 1.1 MB (1064130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57012602ba9a2c6ff0f9f1dd642772602b64f00e422d1e8e61af856666bc23a0`  
		Last Modified: Tue, 02 Jul 2024 22:44:33 GMT  
		Size: 10.9 MB (10920173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b62380eb3355a2f2e477d4a2da22f5fefad98c8c1c1184d45dbf29e0f6717`  
		Last Modified: Wed, 03 Jul 2024 06:57:06 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9657dda8a53fc3369b495c2d7a35206653e5e9e214c82f03a1a54476f95cc8bb`  
		Last Modified: Wed, 10 Jul 2024 19:20:18 GMT  
		Size: 2.8 MB (2773885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a879933737ffb754f82595cffaf02175947d355e352031b54d2162c1d04fd607`  
		Last Modified: Wed, 10 Jul 2024 20:08:53 GMT  
		Size: 3.8 MB (3756224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:12b98b6b5eee9eb0b9944a2dd3ce500e531d5d94b16669460f91493fd7c63ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8988e835e360711c6a4403bc9b4d7c5f4169746bc8fa16461127973b46e2ad1f`

```dockerfile
```

-	Layers:
	-	`sha256:f1d066cc9ad0dba985f8cace2c8ef7aacf7d90d300e860f00744579d832a7e15`  
		Last Modified: Thu, 11 Jul 2024 17:03:09 GMT  
		Size: 2.7 MB (2688724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d5d4e87e5d718694892faf2d56b8cf91c52274e703cd854efe745f0ef4fb67`  
		Last Modified: Thu, 11 Jul 2024 17:03:08 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:6bed323a4b096f944b0bae95bd52d7c8b76722eb10ba54cec33dd554aa3db698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51010700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d7e52baa11f13516ceabf1a681ba2bcaa0947e3219d593ac2c518a65c961ca`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa02f08be8cf5e5b88cd980dd4be0cbb80d4ab51edda74d9606e1513b92c77d`  
		Last Modified: Wed, 10 Jul 2024 19:12:13 GMT  
		Size: 1.1 MB (1088863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74ed87ed2bb26d15929e34cad01876f547f5c31fce13ab2b2db8cea462c5a80`  
		Last Modified: Wed, 10 Jul 2024 19:12:13 GMT  
		Size: 11.0 MB (10983172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b6d71a5d4da738c79d1f22987acb675e81853abfb09bd67db946179d1184e`  
		Last Modified: Wed, 10 Jul 2024 19:12:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411ea0c7d7a907454908cf78bad2a7be23ceca14970e110b4783d5933fa8e3e0`  
		Last Modified: Wed, 10 Jul 2024 19:12:13 GMT  
		Size: 2.8 MB (2773676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688ad501ee29e1e1445f37461026417fb75812a9fa3eef9fb7bd75b6cfbd1ce7`  
		Last Modified: Thu, 11 Jul 2024 16:58:16 GMT  
		Size: 3.8 MB (3756305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:0299ae9b7f75b4d376127de2fd66ce5366731aa92abc673833742b684ac58145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5838113f3bc86d15f3d74d294de931fe9d29d1ab702bd2631ead27bb251d9f68`

```dockerfile
```

-	Layers:
	-	`sha256:80ccb414aab3c7196fac4ba64902be69be8b2da457bf8b0d5e6f7a7a7a077dc0`  
		Last Modified: Thu, 11 Jul 2024 16:58:16 GMT  
		Size: 2.7 MB (2685570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f861690f1b98ca407d0fb8c56f85ba6bc8b42e4e9c357dcb9821fb17cdda6d`  
		Last Modified: Thu, 11 Jul 2024 16:58:17 GMT  
		Size: 8.5 KB (8459 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; mips64le

```console
$ docker pull hylang@sha256:99c1d7f3e93adedcf27da30060dc7346aacfd0ed184fc2f636c7ac1f66143b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48022422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a626fcd981062ed9c205b02593ace0bee0d39ae08c04923ddcd6d4d30414f412`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:38 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Tue, 02 Jul 2024 01:19:42 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3551dda6984f1324dd108794162bc6b119a2dfbc7f88392a8345038ffd45be4`  
		Last Modified: Wed, 10 Jul 2024 20:05:47 GMT  
		Size: 1.1 MB (1050112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0d65f92c12172c9a993a3f1c648c4243e39e0c7029467d3827c2c4040ef2e`  
		Last Modified: Wed, 10 Jul 2024 20:58:50 GMT  
		Size: 10.8 MB (10800681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2369e33b3f608f7ff67f1bf2cac74a6c2fe97eb32c8aa5a9207fb3fb8531b5`  
		Last Modified: Wed, 10 Jul 2024 20:58:49 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98d2af57156d14f10fd7a263f493cb04f795af9357d38936878dbd52781249`  
		Last Modified: Wed, 10 Jul 2024 20:58:50 GMT  
		Size: 2.8 MB (2774722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc62719c4fe48e5b9fd8a353477728aa06064244d01dc505cc544aa58ee432d`  
		Last Modified: Thu, 11 Jul 2024 17:05:45 GMT  
		Size: 3.8 MB (3756825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:4baefc1d09e78c8e243419ce1f5a9a3be2001bbe1ce5eaefc09dfa9664fe3cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 KB (8338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0255d20ffe645fbf4448d98775e4e2ffd3730ef322595eb924678daa3db5187e`

```dockerfile
```

-	Layers:
	-	`sha256:68427992a8e48715ed8151b67557bc4b368ca4e6b24d74bb400c37e73bac31fb`  
		Last Modified: Thu, 11 Jul 2024 17:05:44 GMT  
		Size: 8.3 KB (8338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:e315b568177db79b95889a9553d3a990d1009a0c8ae04af5985936a6cc52e889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54106843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc716888cbc337a7140fa5ca2bdaa50d4951a3091e7a993cf64965205ebacc6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:03 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Tue, 02 Jul 2024 01:18:05 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bb4d7d6f5ea93020aee1c796b84ffdc8197c451898058312c2fe823ccd4b1f`  
		Last Modified: Wed, 03 Jul 2024 12:58:01 GMT  
		Size: 1.1 MB (1094935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b75a9e74d1e74e5789d05205ac60ef118b067343e829c63cc056a6998c2ba47`  
		Last Modified: Wed, 03 Jul 2024 16:51:43 GMT  
		Size: 11.2 MB (11181934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27129397459d191a58e1f5b370279c5bf30f565e076d55def925df4e0eea1e8a`  
		Last Modified: Wed, 03 Jul 2024 16:51:42 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2397170d178667934e17ae74c4a8d4dae03355d2b36214e04c6cd6ad91e4e0e`  
		Last Modified: Wed, 10 Jul 2024 22:34:28 GMT  
		Size: 2.8 MB (2774334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aea98a50211012c80a7ed2fb1a68c956f7ed8a17c6e2c1aa46463987310eec6`  
		Last Modified: Wed, 10 Jul 2024 23:27:33 GMT  
		Size: 3.8 MB (3756219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6c31caf577cf9aca4d80aa50fc79f59f7f815ec70b16e44a19dd9e616f7f20da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ecdd7a1f0270ca63a4b60e70d3d2fed1e2c1f4364fe8dd18a9fea01f0f458`

```dockerfile
```

-	Layers:
	-	`sha256:abc887e5bfc4aa46f3dfee890fc9bd677df22e6f174414316e853717515d765e`  
		Last Modified: Thu, 11 Jul 2024 17:08:54 GMT  
		Size: 2.7 MB (2692841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab447167429232bf4f99a4d2840739ca777308a4219c5a5989a1daafe6dc0511`  
		Last Modified: Thu, 11 Jul 2024 17:08:54 GMT  
		Size: 8.5 KB (8547 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:6ac5a9e8d2a478cba473bdbd590c29772523acf3217831467f3590f4e4d6c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48055933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b591c6b06512b1fc9304005354035f2cc2faf5a61a553354ce0157b591f33a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14220572a7603ca678630a49daa33ea1fc9e1570b0be8aa0f934f8d0d7c8553`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 1.1 MB (1075919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc15fd49f1faaa9d5ce5a6221d3a4b11dbe500b258acff7055faea4e3dffe57`  
		Last Modified: Tue, 02 Jul 2024 10:07:44 GMT  
		Size: 10.8 MB (10787889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cde981a9c0353b4f81f1a2755523d926e3c7940a0bec22c32f401e3285085d`  
		Last Modified: Wed, 03 Jul 2024 06:32:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22427bffc07cfad66d4c2c4dc358f590551a7254212966bd3607ed77f12edf96`  
		Last Modified: Wed, 10 Jul 2024 19:30:18 GMT  
		Size: 2.8 MB (2773503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adbe7ed423d410dfadad5c75326e728aadd92303842095ead183e2b136324ec`  
		Last Modified: Wed, 10 Jul 2024 20:17:21 GMT  
		Size: 3.8 MB (3756039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c7f1e91e67e237fa743741493ebea83528fc6b42f96ceaaaa9a90227c2efb10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6660d8e771b90d009bf3964bbc9f36f248f1daf8087e4386020669cf6e6b0d43`

```dockerfile
```

-	Layers:
	-	`sha256:397e5f6d82fab81a5eb491437878c21b52713ecaa0e3225f5243d5c8b199a9f6`  
		Last Modified: Thu, 11 Jul 2024 17:07:15 GMT  
		Size: 2.7 MB (2688660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96714e00b641e2a068afa874884e9166e06f6c4297ed90351796ecf588271683`  
		Last Modified: Thu, 11 Jul 2024 17:07:15 GMT  
		Size: 8.5 KB (8502 bytes)  
		MIME: application/vnd.in-toto+json
