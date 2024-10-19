## `python:bullseye`

```console
$ docker pull python@sha256:8df22aa26de35be64af239ff203857b9370a1418a732a9d69481dca717f3c3bd
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

### `python:bullseye` - linux; amd64

```console
$ docker pull python@sha256:29849d5c1b2ae2ffb586061d92602edd5ce888f02f9eb6ef1e6f2390dec3cfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356336948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123e9bfcb0d6e2ebd0b464138098e26bd0808ff0f113841837be8b93078f8828`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dcdbbe5c1d62201fcee2dd2ca8ca09ec165f840a8a7a9fe05e7875b49b468`  
		Last Modified: Sat, 19 Oct 2024 02:53:29 GMT  
		Size: 197.1 MB (197069718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d98f36c1a4f89a3b90af2cee7020043d6eb1713693041e7e12772475683b093`  
		Last Modified: Sat, 19 Oct 2024 04:14:56 GMT  
		Size: 6.1 MB (6051638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a8a88abe2da6b2c499a907a12cd9b400c611f2495e5bc52d28dad91ea4611`  
		Last Modified: Sat, 19 Oct 2024 04:14:57 GMT  
		Size: 27.6 MB (27647131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a8855249268936e379a57519b5300ae335566ef052a189a9f1c77457a97a58`  
		Last Modified: Sat, 19 Oct 2024 04:14:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:a3b5824c0b8466d9b7e425924db0ef812a1e576cfcfc28fb7d0b0d540afe7d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15610607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c95e2d7d206834d1fddaf835c84f58ccf291b3c24dbd22c61c59d5df4f42021`

```dockerfile
```

-	Layers:
	-	`sha256:bcdebad4eaced547793cc4265853ae9124644687008b67e42ceea7de97e03765`  
		Last Modified: Sat, 19 Oct 2024 04:14:56 GMT  
		Size: 15.6 MB (15590438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24a73c103372121565afb8d6425a6092a62d55d591d90a407f519b59ca1161b`  
		Last Modified: Sat, 19 Oct 2024 04:14:56 GMT  
		Size: 20.2 KB (20169 bytes)  
		MIME: application/vnd.in-toto+json

### `python:bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:233ada1cc4a036f06f708afad5ef079dc2ba38aaa8603cb0b03e6918fd86ed8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315087358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055d14e0bdbba582a86ca7972dd29691966e57a0a895161e70b73def8ed194a1`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e9a35d7435e132469afada259cc2b810c9b47a2c14559cf5f8650544badc`  
		Last Modified: Sat, 19 Oct 2024 17:12:22 GMT  
		Size: 5.5 MB (5461150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a6eb02773bd4917a3d94cf31a9e2c983217bc54dd90561dacc013b7d6f19f7`  
		Last Modified: Sat, 19 Oct 2024 17:53:30 GMT  
		Size: 26.4 MB (26380671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cec388f331d04093c8e321abd5613be4f585ae65384a3da365f9ef666bcfaa7`  
		Last Modified: Sat, 19 Oct 2024 17:53:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:ed6c24d6f59ee4cad20a770da829b8d5c3f299cc31138d88fa4ffff0861b848d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1916de6082362994d1c8b86668cd2034016608fbdb758e7e571be02a8d87480e`

```dockerfile
```

-	Layers:
	-	`sha256:ab6771d04f762adaeb883ed1eb9357e4e6b3d6411c6c732195e4b4edd5e3749b`  
		Last Modified: Sat, 19 Oct 2024 17:53:24 GMT  
		Size: 15.4 MB (15391004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10225eba14e69d4b353b9e9ed7de43a131ef838eda92c0c44384e6c2a8deddc`  
		Last Modified: Sat, 19 Oct 2024 17:53:24 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `python:bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:c867dd42bcb001127383c8a5846ae075a44cf797f816ee6e83498eed90d1f6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347492892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e1e978c1df346cef46a145a3b78757f22b7170584f138e4f34fa5e00215eb4`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beacd49a41cd1eca48060a2d558ee13b717d3adcb991d77f740ab47970d574ec`  
		Last Modified: Sat, 19 Oct 2024 17:53:45 GMT  
		Size: 6.2 MB (6164891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2472dfb3c6401a0886d12d3cdb74b869859d1b0db74d7557af2c08ce742cb992`  
		Last Modified: Sat, 19 Oct 2024 18:20:43 GMT  
		Size: 27.0 MB (27041167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188fe2e5d4ee165a94cef6faa1cdd97071a66ade6052b1f69ffca0234be0501d`  
		Last Modified: Sat, 19 Oct 2024 18:20:42 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:37df0b42fef31f3f6247c96c6b985cc050e422186831861c8e82944c41038edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afabd36b7443d12e41703ca44df6cc379b1dd2940fde51a3819527413af02e1f`

```dockerfile
```

-	Layers:
	-	`sha256:b83b9f1ed1447a21b173773bb138b5a564c9fd3e8fee645b7a155257cba8cc98`  
		Last Modified: Sat, 19 Oct 2024 18:20:43 GMT  
		Size: 15.6 MB (15592721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef02152803d911d5fa72562be685e54afc8830c4cef2b49d3c991697c4df747d`  
		Last Modified: Sat, 19 Oct 2024 18:20:42 GMT  
		Size: 20.3 KB (20326 bytes)  
		MIME: application/vnd.in-toto+json

### `python:bullseye` - linux; 386

```console
$ docker pull python@sha256:58f36268d6fa3ce2b8f0ba9ceda1d8bb3b3e7882c4e1405880400e597aea4553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361457698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67972e3b646bfdc8dfa507331ab35bccea3d40c2b1306765b1cf5b539a763f74`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668ade1ad6ecf9ecde05517f60eb0af8fbad048955aa9fa5125dfe9e07f656d7`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 200.0 MB (199977836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed6d2ab351ab1919964f3950d99a05fb025f22fc16546591998145ffde6a026`  
		Last Modified: Sat, 19 Oct 2024 04:22:17 GMT  
		Size: 6.4 MB (6441542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093e9902f6572eb626999526ca1db7a639c0be05fedba6c646984b221605b8c`  
		Last Modified: Sat, 19 Oct 2024 04:22:17 GMT  
		Size: 26.7 MB (26665293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775616f226628c2841e34f3e8434a74823e9ec58d05dbe12fa3a20ae40e41ad4`  
		Last Modified: Sat, 19 Oct 2024 04:22:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:29cedd129d14781df6a40f046d8d8b1cd76b3573ff468a4373106b76435366e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15598844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b46f8d4ff071bd966167e5bf6d688ce84fab130580fba901b0278d003017ad`

```dockerfile
```

-	Layers:
	-	`sha256:8819acd50d593f6914b95220d6cc7a48500e68d17a58374165daa32762c553c7`  
		Last Modified: Sat, 19 Oct 2024 04:22:17 GMT  
		Size: 15.6 MB (15578711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4455a3c8b30cc8705d8693df961f48dc56875a548e7f2c85dbef68047cdd8e4`  
		Last Modified: Sat, 19 Oct 2024 04:22:17 GMT  
		Size: 20.1 KB (20133 bytes)  
		MIME: application/vnd.in-toto+json
