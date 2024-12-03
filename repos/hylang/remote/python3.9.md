## `hylang:python3.9`

```console
$ docker pull hylang@sha256:391427aec8c4a3411bfb10190ff55160bab642de7f0b7224299fbdeb97d3c534
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

### `hylang:python3.9` - linux; amd64

```console
$ docker pull hylang@sha256:144512c8025ace39f944389403e5733208cf8dfb4a9e1bd9403bcf813755f17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50149460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf41f6ab1cac0eb38da8bf3aab430595d368a062b948927be889681555ba72`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:28f178de310bc01fac2b8f9b87541563f1a77527ff6c14ee6aae0954864556ec`  
		Last Modified: Tue, 03 Dec 2024 02:22:02 GMT  
		Size: 3.3 MB (3317299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0630bc558f158662d2f804360f24f584b79c9b7bff342b14be6f5945c300d8`  
		Last Modified: Tue, 03 Dec 2024 02:22:02 GMT  
		Size: 14.9 MB (14931108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa04e2c73d5969c08650d34ef8b62680ee75ddf3cef21fe3c65afb938f06f9f`  
		Last Modified: Tue, 03 Dec 2024 02:22:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34d75eacccc78431e521d3c0ab7e25ee899fb59f6b45f0589bacdae0006977`  
		Last Modified: Tue, 03 Dec 2024 03:26:32 GMT  
		Size: 3.7 MB (3669223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:78ef55508645163d65a97a59c57529d3f337eed2e4d10c92363aa782dc30d34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d8ac318f2ecc9dbf16e87d80cb603b5ed37c20941e280446f3cdae8c5b0032`

```dockerfile
```

-	Layers:
	-	`sha256:172d5fdd3920b7c5590c0ddf715a8e7fda44e794a33de886860d1b58f75a59eb`  
		Last Modified: Tue, 03 Dec 2024 03:26:32 GMT  
		Size: 2.5 MB (2466573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b6636682e3eac9dcd9d62521e91784ff4b3c7b336feea2b891ff94e9e4df82`  
		Last Modified: Tue, 03 Dec 2024 03:26:31 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; arm variant v5

```console
$ docker pull hylang@sha256:ca9a6280bbb6b00885fce1a8e5a70fd1fe2049fbf40717f0202a37127a2f326a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46677213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1a63511f3b400e0324a9211e470b959fea0bf2ff529733f6135ee05f5faaaf`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:c5fe562788b001990bcad6bd8ca1525388d447352e500a349930412539d15696`  
		Last Modified: Tue, 03 Dec 2024 08:05:00 GMT  
		Size: 14.4 MB (14362573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f04e697b7896f25d5affa199e800b93e75108c25126c2146ad257e70b8bae1`  
		Last Modified: Tue, 03 Dec 2024 08:05:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aee49d4c130f8e7eb1c84c663c4e116fafa7566c15259ae5120c5767f4a12e5`  
		Last Modified: Tue, 03 Dec 2024 09:56:01 GMT  
		Size: 3.7 MB (3669460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:d9ede93032f1cf1275955eb9a35a64c44a23c7bdff9c7aa22d8ad2bf06557086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41d9e7e664b4603048809b5b5b9a7707bd94110b67126c606653e0ed4d83fed`

```dockerfile
```

-	Layers:
	-	`sha256:a7218a5737284ae472da10d0b114db257f65a75658fd58bdcf0ad20a14480186`  
		Last Modified: Tue, 03 Dec 2024 09:56:00 GMT  
		Size: 2.5 MB (2470116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2dbacd4bf4c23404011569d0cf284f78c32d891cfa46a85eebb93f02ad86376`  
		Last Modified: Tue, 03 Dec 2024 09:56:00 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b0641161ab081e4f9e93f2dfcd361ac105f47757142aec013bd4b0f85807ad04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45256810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59eaf6297cbd20b4275c51bd53a61287bcc760e56ab6cd7489a393e91e3265ac`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:26d1ed493545e705f0a014e7f3418cd6e365d0091d20abb34cec42f0bb5226d8`  
		Last Modified: Wed, 13 Nov 2024 05:43:26 GMT  
		Size: 14.0 MB (13953371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41798b06c1fac1cf96f45e637a84c8a16612bdc1e9c70ec3a2cd171299573313`  
		Last Modified: Wed, 13 Nov 2024 05:43:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f79a5a565a29f0b837736f1cce54beda2590b526bbf4e7c1cf20eb0ba44f51`  
		Last Modified: Wed, 13 Nov 2024 14:58:42 GMT  
		Size: 3.7 MB (3669450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:2602f2914e6ec103a73a58c0dc40e06112bd49372ac58f3a6676d62c8cc34046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabf894e43c7f808048e383e17ec76298ebbb0c4d31b985909636a5870ad1654`

```dockerfile
```

-	Layers:
	-	`sha256:9061f04607c4758b860d5667e9eace664e1ddc3362301fcf3a30593dabc598ee`  
		Last Modified: Wed, 13 Nov 2024 14:58:42 GMT  
		Size: 2.5 MB (2470121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f3a656f1f02e097af5ca155549ce1812063123dfb6525729f241785ddb04f5`  
		Last Modified: Wed, 13 Nov 2024 14:58:41 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4bc556a627e94a47352bddd2c2fed5c545b588559f73992c0eee89e13bde5bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50991368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6537a6d892d64dc87fe191dc0c53a8f2229e02a469168d0238e7296c1ab91dd`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:193e8340ba1de799bd9476ee14a9c4e24d0f51ccfe4c57c82bb7e6f7f807526e`  
		Last Modified: Tue, 12 Nov 2024 23:15:26 GMT  
		Size: 14.8 MB (14832193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a72ce45a2f47cd2b49aa49edba5d1d4c3b2fe18309912991d48b62ebccaa8`  
		Last Modified: Tue, 12 Nov 2024 23:15:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5376e3b90a921c4f7a8e1743f736057e90f086a92a5dc2aa158943831d4c2474`  
		Last Modified: Wed, 13 Nov 2024 07:29:18 GMT  
		Size: 3.7 MB (3669541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:b60eb488d605fa606413ea3912811cf22416f56ec188c10335d51d4f5de4cebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b586c48c9dfadb7772f50cc2373d6a632a600d5f3f19ce324ea4926743fcafc2`

```dockerfile
```

-	Layers:
	-	`sha256:937f50c8d13e02eb3772c38762b152e2296d84df5c2f16dcaf198840c132c8d3`  
		Last Modified: Wed, 13 Nov 2024 07:29:18 GMT  
		Size: 2.5 MB (2468141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1af135c7106fe1c93b5d61fb9443abc0de702c3a962860fb3fb8b82101363de`  
		Last Modified: Wed, 13 Nov 2024 07:29:17 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; 386

```console
$ docker pull hylang@sha256:5d6ace4ca567c91b1c2b11e5188312e4d97b1388096ea967cc1916037756c5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51372102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc1a67ac7dde7930ab1f2efd549d4cfb3c610c191d99469b3462465ba69884b`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:1e41007f4395b035e021d40619dfd5b689ad94bac717cd6ac6a2a1cde6969b39`  
		Last Modified: Tue, 03 Dec 2024 02:36:51 GMT  
		Size: 3.3 MB (3316881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac989d61c7142087f579ebdb3cdfc75794826ad808c3d4b9512820d87daecd20`  
		Last Modified: Tue, 03 Dec 2024 02:36:51 GMT  
		Size: 15.2 MB (15180201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4653ecc74bd19895facd35a68fd886211d77b00ae7f652f0116493c574830`  
		Last Modified: Tue, 03 Dec 2024 02:36:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553442463bd3a195f1495702ba78d182072276e80de168710d46b2b211ee4fb`  
		Last Modified: Tue, 03 Dec 2024 03:23:07 GMT  
		Size: 3.7 MB (3669284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:70923d99f829ab53bc78f99788907494829f048e55a36d5d27e2497d28acb90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67236975bd46a27f4b12eb5f6ab168e9fd636c674deda0189d110ab01067461a`

```dockerfile
```

-	Layers:
	-	`sha256:9c28588d9101e2932c2167ab99eafd49503e02d5bebc3886e5b069db0e6b844c`  
		Last Modified: Tue, 03 Dec 2024 03:23:06 GMT  
		Size: 2.5 MB (2463652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171de8e42ca8238d6659435ea45a235b42a4f41d350601ba86942d4581394ee7`  
		Last Modified: Tue, 03 Dec 2024 03:23:06 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; mips64le

```console
$ docker pull hylang@sha256:0dcca22e83912bc69168e23cc36009d0fc8d7792b2e3cb2e9c7c6cb46b6ee7f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50319081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f9e4739ac52ea5ba18222046c3beefa6b4963063b0d6efd89203d3f72f7f38`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:01c6d0bf10848996e396c89b66742849d41fd852c3610146badf9f612e62945b`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 29.1 MB (29127365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3682a3b0afdfb84007dfbe114c020784a6b702e0c4ee59e7787603cc2a3fda4a`  
		Last Modified: Tue, 12 Nov 2024 23:09:34 GMT  
		Size: 2.9 MB (2907048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459b20e176555209f68e556b924ada8975b51c1876fddeab38f1d9709aa20ae3`  
		Last Modified: Tue, 12 Nov 2024 23:09:35 GMT  
		Size: 14.6 MB (14614279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e8002819708c5c01c1d1553fda694fa86d07d647e68cd5a76be1e9d5709d24`  
		Last Modified: Tue, 12 Nov 2024 23:09:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f4910706bedaf570f0e6c87ab00303595f72958247e33e158b75b2cb955d3e`  
		Last Modified: Wed, 13 Nov 2024 06:55:12 GMT  
		Size: 3.7 MB (3670140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:5b25b03f7dc7034e44eda5d3004a59c7abcb34a50cf8fb8563b512d4e11671bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3e537197fa3b64220cdf9e16bdb21c8e233ba6f09d7382b57ccce3427beabc`

```dockerfile
```

-	Layers:
	-	`sha256:3f3f402aea3c0fb96c48f83263edd3ce710db4dae24b458c27741f64e36f9817`  
		Last Modified: Wed, 13 Nov 2024 06:55:11 GMT  
		Size: 9.1 KB (9143 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; ppc64le

```console
$ docker pull hylang@sha256:e1a68825fa1665f8fd99289e173ed889c91f4e1181c78f5a057bedd09067c06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56047072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e24711e448db60e8d963f62cfe6dbe9e382af1b73044f448562157783386d2`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:4540718b98c18fcb00b635dea8d08bd89464ad9180858ba872e553f06b5e2ab1`  
		Last Modified: Tue, 12 Nov 2024 13:53:52 GMT  
		Size: 15.5 MB (15538121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb5d99ca5dc9d25c7e7c8dd7d210061a8bca1810ddf3e0de730e2c55abd3150`  
		Last Modified: Tue, 12 Nov 2024 13:53:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc3ec904d70aea8d09cea05cca5703225e8c929c5be7787e5662e13606c4343`  
		Last Modified: Tue, 12 Nov 2024 23:29:28 GMT  
		Size: 3.7 MB (3669638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:c1743729fe6323d69dcebbc01aaca06ef3103a2f57537e089a2f481aefee58d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cb7ecc5723ac9970c04fd8cd66cd24f2c6567bcb4d9e35e3d9d292d532530b`

```dockerfile
```

-	Layers:
	-	`sha256:085ff5d7802c1ef31780525341d790e42fab8b6e9a3d454042749c73fd7d21b1`  
		Last Modified: Tue, 12 Nov 2024 23:29:28 GMT  
		Size: 2.5 MB (2472236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c2785a26ee5e4c38698ab2e88487ae9efdb73a7516a80f724c9401a3e78ca3`  
		Last Modified: Tue, 12 Nov 2024 23:29:27 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; s390x

```console
$ docker pull hylang@sha256:e3c4396eb33d80a3766219d6e4d8be314c8561e7afd3ec3c71e92155fc8335d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48249528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c102d01d19cca35444a54cae1cddbc24254af1860485ac89be3fd64378e2e`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.9.20
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=6b281279efd85294d2d6993e173983a57464c0133956fbbb5536ec9646beaf0c
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:309154319c6f0bb13d12122c4d8b1cfab15e126fb9d74113e5279360e8b225c4`  
		Last Modified: Tue, 03 Dec 2024 06:58:11 GMT  
		Size: 14.7 MB (14720095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d168a691993d65464447784e440716675fce9c33080bf54cd86eb98662e520bc`  
		Last Modified: Tue, 03 Dec 2024 06:58:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9f45ef505d8aaf7a2726ea48f6a0f8a1fae6fc24a1ac6c9d3887d7b2a19cf1`  
		Last Modified: Tue, 03 Dec 2024 10:23:47 GMT  
		Size: 3.7 MB (3669422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:2d6ba7b7ae95f4429774990f7829c0fa6e622266a9486087080139c8f97b1d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebc17d1eab83a9814b758d9bc9326bab34429f95407e7198b9f1d35bcc13eca`

```dockerfile
```

-	Layers:
	-	`sha256:7e14834792d877f97b355f997889ebbd5ded9c01cd9d31f4fd5d9afad750886f`  
		Last Modified: Tue, 03 Dec 2024 10:23:47 GMT  
		Size: 2.5 MB (2466282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad4916f052b08378963e9f8af4576405a8ef3c92f678c3a931722bd798c8580`  
		Last Modified: Tue, 03 Dec 2024 10:23:47 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.in-toto+json
