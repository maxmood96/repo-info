## `pypy:2-slim-bullseye`

```console
$ docker pull pypy@sha256:4b610d639b24c2662259bb477af8516ff50d532901f00ebd20f69e094aa04a91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:6a16e7da28d039033611c31cf2a5ceb3eacd53434b61e07f93d3417371756f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64822240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bee1640deaef82dd440b7ab89dd45192265bec7b51a57d9426b19ed501ce9a9`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 04 Jul 2025 16:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 16:07:12 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jul 2025 16:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 16:07:12 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 04 Jul 2025 16:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 04 Jul 2025 16:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed542539eab9c3bcd97656525b95cddf993da168bd64cf51ab024c139bb32468`  
		Last Modified: Mon, 07 Jul 2025 20:58:07 GMT  
		Size: 1.1 MB (1068009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914a221cfa77b323982fbf118d0cf98931063d27335f7dfa684039a83f5f5ff2`  
		Last Modified: Mon, 07 Jul 2025 20:58:08 GMT  
		Size: 33.5 MB (33498184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:05bb475b33c285f8c958af96e07ee5cf55ff5b4c8beb61ee6bab19b5c6addbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2802915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fbf9a10bd51cc0e78f82dbd4f56a1ba1e8ec9954b02820149820374ff3103`

```dockerfile
```

-	Layers:
	-	`sha256:a56b2ddc1d56ec473aebd9c44dae608d32770aa2007b51b900606f9127cd5406`  
		Last Modified: Mon, 07 Jul 2025 21:38:50 GMT  
		Size: 2.8 MB (2784627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fd4e14d86876244c5bbce7cd86e2f6c4b88fa8d009fead2c9c56ac9fecf600`  
		Last Modified: Mon, 07 Jul 2025 21:38:51 GMT  
		Size: 18.3 KB (18288 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:7ce3f9ba436b74bb5da3a7d14e68d47224a91bf0b4d16bbf615c3fc6aac7b81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61209366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a692b821559c73ae3872533398dc74b468894d9ce6c51032aa5fe6438a68e2`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 04 Jul 2025 16:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 16:07:12 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jul 2025 16:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 16:07:12 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 04 Jul 2025 16:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 04 Jul 2025 16:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb34f077ca86221c8cfc5c0988ab8f74b59e74e8f088ea560a8d5617be61e0b4`  
		Last Modified: Tue, 08 Jul 2025 03:02:46 GMT  
		Size: 1.1 MB (1055234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f507cdb166c59ae22735230ee1773d0fd059c52f373162ae66a12da9ed2965`  
		Last Modified: Tue, 08 Jul 2025 03:02:59 GMT  
		Size: 31.4 MB (31409992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:79164fd17ff7ac71452dab5603aeefad48e206af7d0f7890bdde07e5d662eb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2803381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d909b4cbd29e9a2350681ed77e8786e3041127e3c4bfcada1fed77d68e11bc9`

```dockerfile
```

-	Layers:
	-	`sha256:5b464a5e250b5043c7afd3655e9f7970a3481e33e5507fe56ac94baeb1a1bf71`  
		Last Modified: Tue, 08 Jul 2025 03:38:43 GMT  
		Size: 2.8 MB (2784926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140d7fc7574e15d3c938c0f1099dafbddc243f954fcf1c1b3c415a5ed9385ba7`  
		Last Modified: Tue, 08 Jul 2025 03:38:43 GMT  
		Size: 18.5 KB (18455 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:d4194aea608d740e6f5c2772a09d7bc2996cca674fa9375f53ec98bdb82e47c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735fa9282e06440aecda472649de6a86c62088e333eecec83ae5babe83508545`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 04 Jul 2025 16:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 16:07:12 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jul 2025 16:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 16:07:12 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 04 Jul 2025 16:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 04 Jul 2025 16:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5db3d0444d71ce7ea4dd08e8d1711f28b7dd9a5a7f5bb2524f435db39a458a`  
		Last Modified: Mon, 07 Jul 2025 20:58:24 GMT  
		Size: 1.1 MB (1080117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accbd1605f12cbcfd26a199639196fc3ca4c1726c05f3abf9f322a4feabc8766`  
		Last Modified: Mon, 07 Jul 2025 20:58:26 GMT  
		Size: 29.0 MB (29032311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:41f713d072ae658151cc178c0c5796a27b68d344114e312b834ccfc099072b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2800020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6169d652ceffe0ad21dfcf9e3f26f9b7c7d17b0f4383bf618c13620616fbd9`

```dockerfile
```

-	Layers:
	-	`sha256:9a05b59b888fe1e10ab3569f67f2c583ce602a03874191205cf485ee6c30a76f`  
		Last Modified: Mon, 07 Jul 2025 21:39:00 GMT  
		Size: 2.8 MB (2781786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477ff562f905216753fd4d3ae81911e630419b456912b9527be558649971e415`  
		Last Modified: Mon, 07 Jul 2025 21:39:01 GMT  
		Size: 18.2 KB (18234 bytes)  
		MIME: application/vnd.in-toto+json
