## `hylang:1-pypy-trixie`

```console
$ docker pull hylang@sha256:70ee13841bb38dcf5004fa5fd7c531a0557ab66aaf68a15929572081ace9db8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:e7ea42cfdcb1bd1bcfaef241276b34e742799330d07ab7961943c7cc5a1dcc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75267973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1785b0c267fc816b620b3aa4af85d9f411f4168b2dedb6d974124f620027ef4`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Aug 2025 20:00:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
CMD ["pypy3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4753e1cd4a80ad9c09d316f680069dccd1a9caad49fcd4122a119500cb1e5b13`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 1.2 MB (1220402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60d67a044be328237e6904f595f4c6e5bd88b163726b38eb838ab121ce781c`  
		Last Modified: Mon, 08 Sep 2025 22:08:25 GMT  
		Size: 37.8 MB (37838896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0254e71461292a8156727f560853fab2da20fa16427870b33a753c7506cf22`  
		Last Modified: Mon, 08 Sep 2025 23:04:01 GMT  
		Size: 6.4 MB (6435180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8f70d0d31854a4751130746190affd224b317d09037d9ca144bd258f687c0d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd5605560a6b67b33dc1e949b40391f746c6c39f0e598d214beacc8bb4d2cc`

```dockerfile
```

-	Layers:
	-	`sha256:b668a3eb8e125f39c3441aea0a27f34c3358d6280f838d48bff8c4b6597a2533`  
		Last Modified: Mon, 08 Sep 2025 23:17:52 GMT  
		Size: 2.2 MB (2236326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d71ae31afb569c8d583a891524207bc61b0caac6b988cae0ffa054b9ee3d8c`  
		Last Modified: Mon, 08 Sep 2025 23:17:55 GMT  
		Size: 8.8 KB (8793 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:10406f8dfb9003ec880c9cf66b2ce1a706614f0f4ccb9fe086bdcb3c73f9652f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73929685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a7206a1deffbb9a152f331c0ec1cd9ea24fd0e5e4f7950001a7d53c490d493`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Aug 2025 20:00:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
CMD ["pypy3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17719d57a6787a5ecd190190fea3ca43f63ce2a836e3822888dd6461520c2710`  
		Last Modified: Wed, 13 Aug 2025 10:18:44 GMT  
		Size: 1.2 MB (1201931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99ced72b32f0c97bcab2ba107c3ffd42b71d2e5db59e2b52522518a68e933c1`  
		Last Modified: Wed, 13 Aug 2025 19:00:19 GMT  
		Size: 36.2 MB (36156359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514d907c3d92c5d611576841a1d65799278116064fc4a4904bbfcb42088cfd9b`  
		Last Modified: Thu, 14 Aug 2025 19:07:49 GMT  
		Size: 6.4 MB (6435351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:e13cb8f8691653151362350a68f4f3275d9a2d96cdd09bad765c692a65e5b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772e27bfb3b7f6a9f289acc4659b994e162ec3da499cfe0f568ad8d8f397c7ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc64bbeb9d2ccd0b26670006d66c20af0db7495c905a7c93d15b9275fab9e8a2`  
		Last Modified: Thu, 14 Aug 2025 11:17:51 GMT  
		Size: 2.2 MB (2235793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4046199098a9acc34f83e73330758c60417827f3c688bafe1f4a3e2c4cb7b1b6`  
		Last Modified: Thu, 14 Aug 2025 11:17:52 GMT  
		Size: 8.9 KB (8945 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-trixie` - linux; 386

```console
$ docker pull hylang@sha256:b4906437439184bac917fdb234165a4285b59488d7281a23f754603a1cc4cd4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73189566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0313fe8409d61d19b62a1880bbb4f1555e2a23d0c1a5cdb25fb887082f29279c`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Aug 2025 20:00:48 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
CMD ["pypy3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3968a78bf374dd8208ef8eb83f1086d025472c116304a84fcbb69f7b441fb2`  
		Last Modified: Mon, 08 Sep 2025 21:58:23 GMT  
		Size: 1.2 MB (1227875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44ee4f2b5971c26f9451ae61b95d354c52cd5a8ed7751dfbb3f03b7c623bd5e`  
		Last Modified: Mon, 08 Sep 2025 21:58:25 GMT  
		Size: 34.2 MB (34236735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584abcd705d7d899e4ab5eb2656e8052770a0908d62a2fa859f6f4318a34b29e`  
		Last Modified: Mon, 08 Sep 2025 21:59:04 GMT  
		Size: 6.4 MB (6435172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:9cf7c203c308b72abeeefdee4280950af8702d680dc9408c8cd47531b0828345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77242e839e5edb6a2086ac255e8d59e0356459c99176c83dfcdd50ebcf33f38`

```dockerfile
```

-	Layers:
	-	`sha256:da83ce1a61d39b33fc2c7d438a5a2c2bf826d9cdea5daa5bcf662fa86464d377`  
		Last Modified: Mon, 08 Sep 2025 23:18:03 GMT  
		Size: 2.2 MB (2233485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a0803ad99205c261ca171890bd74d0fa88a1a82a9d9362b85439938ed5fbbd`  
		Last Modified: Mon, 08 Sep 2025 23:18:05 GMT  
		Size: 8.7 KB (8741 bytes)  
		MIME: application/vnd.in-toto+json
