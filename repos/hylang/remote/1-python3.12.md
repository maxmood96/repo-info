## `hylang:1-python3.12`

```console
$ docker pull hylang@sha256:b3459296bd2df4755afe62a95ffb60669e0f58ab49007016c9868ce095a6b75c
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `hylang:1-python3.12` - linux; amd64

```console
$ docker pull hylang@sha256:86e524584dd408c0173a9f61a5307a2239346d927e0375dccce75ea1f0adcc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50762434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ebccea0b6c5ddf2d2c3d4d0d9d75ad6375201051b59ee174c95b9962ca29a8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e739003c33414360cf2cec9452e1935b1bfcae79f279c33009bf4c0d5596f52`  
		Last Modified: Tue, 03 Dec 2024 02:29:07 GMT  
		Size: 3.3 MB (3317246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f86e0092844f78afa84a3b63059ea82e82fa93a28eedde55386370d924e8cf3`  
		Last Modified: Tue, 03 Dec 2024 02:29:07 GMT  
		Size: 13.6 MB (13625510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46271edb89aec00565d974118707aaded82928c7ea7cb0a2bcc94b1f17e17e3d`  
		Last Modified: Tue, 03 Dec 2024 02:29:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5267b1d6ae91f1c51c831f1095bf4280bedc8b371e477b9ef7f1c594e94c9e`  
		Last Modified: Tue, 03 Dec 2024 03:26:33 GMT  
		Size: 5.6 MB (5587849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:22f02fe8d595dbc9ac07edacaac8c6f2ab54ccb5449b2e363ed6bbf13353c3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18680be11f2fc4b0261171056800de33dbdb92f348a5dd379834a71faf3e44`

```dockerfile
```

-	Layers:
	-	`sha256:d155edeaa961b32bc62cbc2962412f51b1d9643a105f4ca850c7dc0bce2b0de7`  
		Last Modified: Tue, 03 Dec 2024 03:26:33 GMT  
		Size: 2.5 MB (2461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c7a2cbcf9b28f339bc8cbf59beebdc41ef51c34bdc06b28b12c8a77914e923`  
		Last Modified: Tue, 03 Dec 2024 03:26:33 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; arm variant v5

```console
$ docker pull hylang@sha256:63a27846db3ea96d1ce42557feedf582c6a25dd2720061be10c007c38a3e4377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d158bb5e8bd9de15e1c203221bf5f18ce3ffc04fec0be271d2998156b31d531`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce20c4e66ffa1764742e2df6279cf58e8b7ebdfaf2f9fb30499a842e87e2036`  
		Last Modified: Tue, 03 Dec 2024 07:27:17 GMT  
		Size: 2.9 MB (2890005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37df92a34f6c4a9aec8ef1302beb489f517d2654bb7645465933c62ca179ba69`  
		Last Modified: Tue, 03 Dec 2024 07:27:17 GMT  
		Size: 13.0 MB (12994548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b09da5e15c8e8c764058f5636cabbc887a3f9def07849db9887ab49a165a1`  
		Last Modified: Tue, 03 Dec 2024 07:27:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f82861c140972cfc51f59fdb8664fbd49719f132dab1c70bdff7fad881ae4ef`  
		Last Modified: Tue, 03 Dec 2024 09:54:25 GMT  
		Size: 5.6 MB (5588421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:5ce3bb4bc06d50bd0b679235e47877753c0afeb359634af2b2392e735b08e4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b410cdb926aafac65ac4d579d29d9ce2fccd85c5dbec78a70659334f54e7434`

```dockerfile
```

-	Layers:
	-	`sha256:6486d16f3763056c8d81aaabe8cb1b48658fed03d7818bd99b8686148f3cb45e`  
		Last Modified: Tue, 03 Dec 2024 09:54:25 GMT  
		Size: 2.5 MB (2465321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4773404040851d21ea40d76a8cf1e5a60bea46ebe72f01b509dd4f9390662d7d`  
		Last Modified: Tue, 03 Dec 2024 09:54:24 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; arm variant v7

```console
$ docker pull hylang@sha256:dd16503a846b4f43ecfec1cc4a76cc3265c2152d62322ae46bfc2a2162388fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45804568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b17411d79cd07f1ea0adfdfa41f4ad95b66c5342202f9e566d5cffd4f7d65d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e21eaca80965f4554a60362cc92686f6d98c8d45dbf96f9be543d0c99a72724`  
		Last Modified: Wed, 13 Nov 2024 03:36:27 GMT  
		Size: 2.9 MB (2914830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c066a65280190a82ec91e1a2bf3a182de909f76e05e7dc58ec124cbef64f21`  
		Last Modified: Wed, 13 Nov 2024 03:36:28 GMT  
		Size: 12.6 MB (12575807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903f35672222efeafa023c81bafc9f97c59eb9acc66bacac5a510c5c6aae625`  
		Last Modified: Wed, 13 Nov 2024 03:36:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d52b5acf9b773f39ad5c98c3a1b2d3f16c3d16c33377f34794a5e2c82dc9c`  
		Last Modified: Wed, 13 Nov 2024 14:50:26 GMT  
		Size: 5.6 MB (5594772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:39a6dbbc44d5067aa8e4577cf607f5423423b81eb6ac06ead0ad579d838a6e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e2f32924f95f24451bb5f5d067ac51e19b7f9c06f12295eaad6e6c5982fcbb`

```dockerfile
```

-	Layers:
	-	`sha256:f61b49a5d0f7d8cb680716ee4d7ed40b198af7fb774fe8200f150b62d2e041e5`  
		Last Modified: Wed, 13 Nov 2024 14:50:26 GMT  
		Size: 2.5 MB (2465326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f2f0456d0ea1326b61a54958f822ffb39869c79e7a35bbaff54d144ab2ee0`  
		Last Modified: Wed, 13 Nov 2024 14:50:26 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4480ae0c30a7bf08af96749a2bbf2d9adb8c97ba1c4be675da74a42206012c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51607561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf76a0e0b82051c6b2a578ee7cb544d01cdfeec18d93d58b8ae39ab2896ec1`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fab32a80202b33cfda04522829fe2e08e9c3a1a4a548a71a09d35720709a5ba`  
		Last Modified: Tue, 12 Nov 2024 21:45:27 GMT  
		Size: 3.3 MB (3332029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00792271782fe07fe1d2b77df4540688555e3239e2632ee3edb2fec39447425`  
		Last Modified: Tue, 12 Nov 2024 21:45:27 GMT  
		Size: 13.5 MB (13523037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c346b5eca8ef1ac8b1963cb55a89e14fe2584c471772627628ead3d8f344d3`  
		Last Modified: Tue, 12 Nov 2024 21:45:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1319af8b1e5bf85bd932a699ff105df3fab5b9a8f6a34b3ffc435c88e4ce31f5`  
		Last Modified: Wed, 13 Nov 2024 07:22:01 GMT  
		Size: 5.6 MB (5594889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:4487ec13f5206b215de1afb8b479c2dc3976044d9ce13f9ca2ecbe6bfd233f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d330b1fdfb52f2754b5119e3d394eab43ac3b691fb2981b20a095aa71d45bd2f`

```dockerfile
```

-	Layers:
	-	`sha256:1ade0598cfefa9120aa674bab51a8909145bd119f6ea99ae29b5fdcd921b3faa`  
		Last Modified: Wed, 13 Nov 2024 07:22:00 GMT  
		Size: 2.5 MB (2463346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:747bdbb8b625fa1414621a149fa125c45da41eded0b2e4ed1c5ddf9e88a1fc2c`  
		Last Modified: Wed, 13 Nov 2024 07:22:00 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; 386

```console
$ docker pull hylang@sha256:8a3feb8398e2c7b39f784ba3ebfdfe6e10c5a7c236a8a62890b56cc77450d9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51995843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7468b8bcff0d1fd6c9a1d432b4fe01c4369efdc92a5a33304df4774c3a196c12`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63203c5aa3243133d5b9371734f8d6534959cedf1f3f0ca44dc0c681d6637525`  
		Last Modified: Tue, 03 Dec 2024 02:45:15 GMT  
		Size: 3.3 MB (3316839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fb6e0107a1ca699501dc541e746b6e6183c0f4b03e59144e8a58f75ab672dc`  
		Last Modified: Tue, 03 Dec 2024 02:45:15 GMT  
		Size: 13.9 MB (13885096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4335f1c0d4f8ccf6637dc36d060f74b3098d6ed26a9f352763a1db23512fba`  
		Last Modified: Tue, 03 Dec 2024 02:45:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c5440b8ae46cda71e6fba7b71607497e11a5016d04c9b1bcfc520b1f65749a`  
		Last Modified: Tue, 03 Dec 2024 03:22:56 GMT  
		Size: 5.6 MB (5588172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:eb5d26b579a76d4ef03073da77077fb0ded7322d2edd4eb6d2a75c954acdd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194efcdd33c4bfedc94b0e2942554ffe584006f14a0af97dea107fe36319bfaf`

```dockerfile
```

-	Layers:
	-	`sha256:e13874044f5e8ae2fd9979f790bf7eedffa8a55a6ddf689c34f880506436817e`  
		Last Modified: Tue, 03 Dec 2024 03:22:55 GMT  
		Size: 2.5 MB (2458857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e125fdaff5521eb2451f9f490818e2c625e6b810b82a6b5d2050f5ee3c1348d5`  
		Last Modified: Tue, 03 Dec 2024 03:22:55 GMT  
		Size: 9.2 KB (9224 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; ppc64le

```console
$ docker pull hylang@sha256:7e94087682787419db29c6ae25942592de829205ebc8ac8bc99cc9f07f9b7696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56702242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e119e1cf1232efd44292aaa88b579ffa9100bbe80cdeff3d919f3832ae7163df`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76890df8aa1e1b13dd45d5481649f929e48f05b16e27df4939ea9229c8b2bed`  
		Last Modified: Tue, 12 Nov 2024 12:38:36 GMT  
		Size: 3.7 MB (3713709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9ad68a1f92499bb10c95887aca1da131503ba5176edd37e67b40c74dd63432`  
		Last Modified: Tue, 12 Nov 2024 12:38:37 GMT  
		Size: 14.3 MB (14267916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d84c2933a739ecf095ec7a313bc2b378bb1a20c6c406c37f7f1a06205ee44`  
		Last Modified: Tue, 12 Nov 2024 12:38:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e37be5a39cbd229d64f374d8a4a02bae107dfb319bc410376a46cdad3861c`  
		Last Modified: Tue, 12 Nov 2024 23:20:12 GMT  
		Size: 5.6 MB (5595015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:4d97ab1b7d2e05abc29c92083028f4c1cba0b65758b2dda619674377e32fd46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2476785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c14f736f6a9f864f1fa322df89fc59e00af03a3ff4829e7de425a526d66c576`

```dockerfile
```

-	Layers:
	-	`sha256:d14795705426fdce2410ae0470e78821c350dc4c777b344d1292f0d4173ee3c9`  
		Last Modified: Tue, 12 Nov 2024 23:20:12 GMT  
		Size: 2.5 MB (2467441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824a1c6ad4b9773b316a244854951b179f289c76fb98dec4fa8cf3407d5a2b3d`  
		Last Modified: Tue, 12 Nov 2024 23:20:11 GMT  
		Size: 9.3 KB (9344 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; s390x

```console
$ docker pull hylang@sha256:998d06ed82de0845d1f3b9d787f3d17ec93cb70c110007aa64ad4928ac245a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48889871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31cc259518fa8b24d78367f4066fc420fb26d70d4b49508c21009c1d84edb8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=24887b92e2afd4a2ac602419ad4b596372f67ac9b077190f459aba390faf5550
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e060c6c4e7ea69f8ea280fa8a0b48f72e5a9cd7a445ea87d0a7a5d70254957`  
		Last Modified: Tue, 03 Dec 2024 06:29:22 GMT  
		Size: 3.0 MB (2980790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8e1fe84e72f851b4f7e4246aac8ab9e32bb677121744a6440b4a8121f7abe7`  
		Last Modified: Tue, 03 Dec 2024 06:29:23 GMT  
		Size: 13.4 MB (13441629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc195707f17b38f1cb60f252c3c8505cff43135b6206016096640e216a849912`  
		Last Modified: Tue, 03 Dec 2024 06:29:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270d2377372419746ebb16875d16d6926728c8c4153de58f0cab26e748987c9`  
		Last Modified: Tue, 03 Dec 2024 10:22:27 GMT  
		Size: 5.6 MB (5588231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:0766058e080657ae0480ce02ba4065f8690812d3607d0fc478333b9b2f8b2dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703430888c9423c758fe5aae8adbb37a75a7396d3aee2d147e24c98b07912ad6`

```dockerfile
```

-	Layers:
	-	`sha256:902e655150566e560e9bec821424e9ef2d0d1d49b72c543f58e8237c08acf10c`  
		Last Modified: Tue, 03 Dec 2024 10:22:27 GMT  
		Size: 2.5 MB (2461487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ed3f970d7ce55b17fc86b0910f3d1f00c39c5a4e5893dd8adf0f0d253723d1`  
		Last Modified: Tue, 03 Dec 2024 10:22:26 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - windows version 10.0.20348.2849; amd64

```console
$ docker pull hylang@sha256:a4bb732a2b9678893de7770286a85896f93d4252fb322dd4e2fb8e75a4bb3306
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320566641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c4ee28b515bb5fe41920d5edb7581f5563585c1e28173eb26cf599f983f36c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:11:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:00 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:11:01 GMT
ENV PYTHON_VERSION=3.12.7
# Thu, 14 Nov 2024 20:11:02 GMT
ENV PYTHON_SHA256=1206721601a62c925d4e4a0dcfc371e88f2ddbe8c0c07962ebb2be9b5bde4570
# Thu, 14 Nov 2024 20:11:38 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:11:39 GMT
CMD ["python"]
# Thu, 14 Nov 2024 21:22:10 GMT
ENV HY_VERSION=1.0.0
# Thu, 14 Nov 2024 21:22:11 GMT
ENV HYRULE_VERSION=0.7.0
# Thu, 14 Nov 2024 21:22:53 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 14 Nov 2024 21:22:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01341484308679987686e83b0177ef97a99af7ae1c6a0fbf117da300d18cdc57`  
		Last Modified: Thu, 14 Nov 2024 20:11:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930337e79cb9ae0089d3cfabb7f3f75d1e3a04b66cd1c33ba5979ce3d6337e29`  
		Last Modified: Thu, 14 Nov 2024 20:11:43 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f148e37c65be2bf9d13abcadeb5c6a447ba2ee0ceca3bfd90eba660680f147a`  
		Last Modified: Thu, 14 Nov 2024 20:11:43 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93246d1429b8f5178d49b7d2cf3830d1588c98cd03b2e54ea54df80b5e658e36`  
		Last Modified: Thu, 14 Nov 2024 20:11:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0591e7de6fc955e8e7443ce9e4151ca57491e4593779c1d64220762334af29`  
		Last Modified: Thu, 14 Nov 2024 20:11:48 GMT  
		Size: 59.6 MB (59574468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b440abedd852266c3f019149c3bc587a3192b038815ab9097be80be2004bfe`  
		Last Modified: Thu, 14 Nov 2024 20:11:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fabcc298f7b68c5ae472f4dbe42e7514385ed38dec9af4647f41f32a3603516`  
		Last Modified: Thu, 14 Nov 2024 21:22:57 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22259c82c5005d1f2abe4a0919641732eaf154b15c35424fe9e3befc8f4ac909`  
		Last Modified: Thu, 14 Nov 2024 21:22:57 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9b9fab9ac3812765c683a07a9726299dc9389bb066e856289d6b1f65ccded7`  
		Last Modified: Thu, 14 Nov 2024 21:22:58 GMT  
		Size: 8.5 MB (8497663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1c9c45cf63e6629003aa0276d7087de9f68ee3e2f8ce1a0f4c906cff5a0a87`  
		Last Modified: Thu, 14 Nov 2024 21:22:57 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.12` - windows version 10.0.17763.6532; amd64

```console
$ docker pull hylang@sha256:74649db9618d5969deab26af0e47a39a8188da61afda8667eb0d7d24328bcf66
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076214183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607f4f1edde526c067b31301b0303405a807715b59ec86be4d7d2245820542bc`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:19:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:19:22 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:19:23 GMT
ENV PYTHON_VERSION=3.12.7
# Thu, 14 Nov 2024 20:19:23 GMT
ENV PYTHON_SHA256=1206721601a62c925d4e4a0dcfc371e88f2ddbe8c0c07962ebb2be9b5bde4570
# Thu, 14 Nov 2024 20:21:05 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:21:06 GMT
CMD ["python"]
# Thu, 14 Nov 2024 21:21:55 GMT
ENV HY_VERSION=1.0.0
# Thu, 14 Nov 2024 21:21:57 GMT
ENV HYRULE_VERSION=0.7.0
# Thu, 14 Nov 2024 21:23:22 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 14 Nov 2024 21:23:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f57c6b8857127fb0a81aa3d37e3349d112d9a6a517734fcb303a2b82b7828e`  
		Last Modified: Thu, 14 Nov 2024 20:21:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ade2f63adeafa487862b5dd740a7b0ab78cd68d8597c4b475dd10756f9f890`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edea0c4bcc8da59dfa3f1ca5a3dce6538509dd728771a10525caaa6d1e656e0`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983073e5013af0f2ee351d083006453d2c93f7774c701a8e4fa7b665571b1573`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66ea5021b948223efe2a1d076ce7d8b71d47924d8e45d2886c81f0585486ad`  
		Last Modified: Thu, 14 Nov 2024 20:21:13 GMT  
		Size: 58.4 MB (58412604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5becb9724dbbe3dd12e0efbb51b2f7ec74880ad32531395585db6c03cec53622`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9482bcab40eb92b4195b243d36f9029f6727a899804c32426e2b8b4b6aa2491f`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b85eb396747ca0f0beaa7336e79156c57e51d67785ac31cea155df7fa0edbf0`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3e133cde516070f885c5ec7a146c79ba856a6ff330df836bdd40c6b9395764`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 7.1 MB (7137409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2edad7cd5a1303447d1bd1e2c9f5a9aefc4f4605f38a89e2187ba4a9a400e`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
