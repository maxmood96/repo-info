## `hylang:python3.9-bullseye`

```console
$ docker pull hylang@sha256:11027d59181338bcb0623f86c8a609811e5a4d26416423bd428b1e7ce9c14400
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:python3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:ba4ef3d09a05e09e99d5fff7c663e1ffc83113afad620c3a09d287a051c8199b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55779981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c25b09420194030eebb2e613404e4ba5a0bf147711fd1c93b0a1679c67e651`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73f192af764b3a80e39df1770514ff2ac322f290012ef57c31aa7177ab0fcf6`  
		Last Modified: Wed, 04 Jun 2025 17:12:44 GMT  
		Size: 1.1 MB (1077894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d41e3f1ea74362a2e45b90f7babc2f017b4e7bd77401d2dd1af9624d04c9d`  
		Last Modified: Wed, 04 Jun 2025 17:12:47 GMT  
		Size: 20.8 MB (20773861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cba455026ee0b49e7a94137585fdabbf646ee26aee0a27618da2e30df469d09`  
		Last Modified: Wed, 04 Jun 2025 17:12:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bbc555deecf50465abe49fc12613039671d512cececb7f1990c248bd8981a3`  
		Last Modified: Wed, 04 Jun 2025 21:20:30 GMT  
		Size: 3.7 MB (3672036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:bca4ed31e25aebbea46f2f7c1434cfffcc739d10a587ee0c7b5052511b6744f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3c7f33456e7834659487b70a4ba241586b9b5fe4d161a1465dd4cefc872f13`

```dockerfile
```

-	Layers:
	-	`sha256:409ce1f96519f3e42903f8fea896562703da254fbfc90bf31b9abc63bae66b63`  
		Last Modified: Wed, 04 Jun 2025 23:26:02 GMT  
		Size: 2.7 MB (2738981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066fc1a1d21129a34704b66ec495201c84175ce0cc6e029eeb2fa47a04be8e4d`  
		Last Modified: Wed, 04 Jun 2025 23:26:03 GMT  
		Size: 8.0 KB (8017 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ff95bc6352ebee6aa17380b80c78c5db281cfa1883219f94a207604e5172d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48720772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0de17665ee2a0755b463a783c7cef018162a8266ea099d6f16580cd3ba032f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d77e6172c26b4080a501eca67ca27311fbd0dabd85e4ad4d0387ce4631519c`  
		Last Modified: Tue, 03 Jun 2025 13:50:35 GMT  
		Size: 1.0 MB (1042868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966bcfd883b4ca406f87a8657baecd1749f6cbbc47e144472ea38a21627f99b`  
		Last Modified: Thu, 05 Jun 2025 00:21:00 GMT  
		Size: 18.5 MB (18461702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01c77b26123ac56cc649888d034f0799e02b805ee8163228daa4b224620ffd9`  
		Last Modified: Wed, 04 Jun 2025 23:14:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802c10ec4bd5e658d5cf9fd134865b088cb8463c0435ce0ce64a36b848382c1b`  
		Last Modified: Wed, 04 Jun 2025 23:51:36 GMT  
		Size: 3.7 MB (3672051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:1b2751fd9cec6c31b2f2c89b5e33789611c4ce3015609b9dc4001f9845ea38c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daefc29973206fc3ed8a24516f80cd6266025043d2308804542f7e7b33713fa`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4cb86feef43f0b8d6649136a0af7d1384104e59ebcd742179ad773bef212b`  
		Last Modified: Thu, 05 Jun 2025 02:20:18 GMT  
		Size: 2.7 MB (2742822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274609614b429601e151b3b0439bd05815538e22160fa3d33471cd558e59874a`  
		Last Modified: Thu, 05 Jun 2025 02:20:19 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:988eaa1be9cb1adc068990ffa2935fa1ad1d49555c3a70ed7ca584607cb8f4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53350754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a94576457ace147e4f458cabe8138bc2576cd9ac1d4872f02aadaf30e989c38`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f68d4647786cc15bd979e88aef7c4edf03f28557e1b55612599156bdb92f7f9`  
		Last Modified: Wed, 04 Jun 2025 19:02:33 GMT  
		Size: 1.1 MB (1065725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5796afdf1a31219ad813d68775d40d6d45eb7e19e8c328ad81543c84bc5ca313`  
		Last Modified: Wed, 04 Jun 2025 21:14:41 GMT  
		Size: 19.9 MB (19866445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac74613f54289253ade2a19a8cc50b59c3ca10f4bcb74dab728f2ef1d0561631`  
		Last Modified: Wed, 04 Jun 2025 21:14:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711e2e1746a492dbd79ed289534fd918c1cfeba8077a642a5abb193a9edd0962`  
		Last Modified: Wed, 04 Jun 2025 21:56:24 GMT  
		Size: 3.7 MB (3672078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c02d14a3acbbbf87eddaea4ba203b4ee6286d9101cf67ad61974743661a3916c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e822548f5ee610f8eb92d0dc3b1658a30c63f6e92bc05fa255aee7ebea206ab`

```dockerfile
```

-	Layers:
	-	`sha256:a9558d954ac8072e6a4fce9e18efe6282ca1003295e7ab161f946dbd84f3a19b`  
		Last Modified: Wed, 04 Jun 2025 23:26:09 GMT  
		Size: 2.7 MB (2739240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cfb6fe0340b6e0ecf427dd1e536fbf6433b318f9eb45d97c5bfb104d0ddd8f`  
		Last Modified: Wed, 04 Jun 2025 23:26:10 GMT  
		Size: 8.1 KB (8121 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:56d11833511bb387c0b72e82d57a8df2821d82d2e43a1afa4df44b4203a18853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56406074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1690d1fdc81460d141aaf13cd8b49298e7d3962059673dd566c979718f4398d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4532c2801497bf6966e95466ee57f4347d562acb96f05e3d6e9e1bf164c05d`  
		Last Modified: Wed, 04 Jun 2025 18:03:27 GMT  
		Size: 1.1 MB (1090540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02a9041446501854be7b251e5d8122744946500849919b786a2ca845952599c`  
		Last Modified: Wed, 04 Jun 2025 18:03:30 GMT  
		Size: 20.5 MB (20453983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734cebbc40cd5a0f40697975b45c133749f11d0bcb7a979c5d26b5ca5ec692e7`  
		Last Modified: Wed, 04 Jun 2025 18:03:27 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc97bc6b573db7d1288b9b98bf7116207c2f64695014623df495316ce223c7`  
		Last Modified: Thu, 05 Jun 2025 02:17:01 GMT  
		Size: 3.7 MB (3672102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5541ce3c1eb6a9d0a6b97e0bee8ead3637082233f70139bc096ed8c755f59225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a9738bb4cee30bbd98241a69b5a8805bdbc234925c45bbd482a0d5369d4964`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f02a6fbd544bbf9f684c989f3d82e11e4d34245c2584b483e9d84dd9a1d05`  
		Last Modified: Wed, 04 Jun 2025 23:26:16 GMT  
		Size: 2.7 MB (2736144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550045f78acc1f319d7131ecbef42f325eb680571f72fb2537b0dc310c0f68e8`  
		Last Modified: Wed, 04 Jun 2025 23:26:17 GMT  
		Size: 8.0 KB (7984 bytes)  
		MIME: application/vnd.in-toto+json
