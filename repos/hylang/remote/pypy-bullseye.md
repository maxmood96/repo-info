## `hylang:pypy-bullseye`

```console
$ docker pull hylang@sha256:b063ba46459ca1922cb9319fd09ac173ad3d5008fae019c2f765f697507ece66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:119df380e240688ae6331fdcd4b2a6d8702f2cc8bf5c063d2099260a5136bfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72150629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82894b2de43be9e0340eed2a63c7c9d8c03de20459dc7de6d53f35b27f6e480`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["pypy3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167f84f040d3c38ba43b25314a8928f3fa324fd2629db8df281d0808e45096d6`  
		Last Modified: Wed, 09 Apr 2025 19:05:08 GMT  
		Size: 1.1 MB (1066601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a178045c370d21fc49cfcee07c678019094039d0f3a4d21984ef123c887a4b`  
		Last Modified: Wed, 09 Apr 2025 19:05:09 GMT  
		Size: 34.5 MB (34463423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c61027f56580dd6a86a40427f6e52736c7158a2215182f7f39ce6fd1281ab9`  
		Last Modified: Wed, 09 Apr 2025 19:08:06 GMT  
		Size: 6.4 MB (6363186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:b3108aa02fa5c9da549033427ebea2865bb10ae686ecf5fc16d5b2ecd006befb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99128d0412530435dad7fc8374d66cc9306cf62313280645c173c0d89ecb6d7`

```dockerfile
```

-	Layers:
	-	`sha256:45646622aaba818a88851cd0479b41fa0596acb0b404138c0183cc797c51d7ce`  
		Last Modified: Wed, 09 Apr 2025 19:08:06 GMT  
		Size: 2.7 MB (2700549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4620619e3bd0947aaae53003f33761db995ea128bad53c9b6e3f4ff31c82a0c`  
		Last Modified: Wed, 09 Apr 2025 19:08:06 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ea2af0dd9d6341441e9180225a96f262fcdea602eab85e27042a0d49da7131fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68904779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced09cf92e80fc5ff0b25621b2a0e307f4d24c2788e870d00bb8fcd61d2f4b86`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["pypy3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaf6d66dd959c9c66f3495115a4e75f6fe552dd36642a1c6297d9d01969466d`  
		Last Modified: Wed, 09 Apr 2025 21:19:09 GMT  
		Size: 1.1 MB (1053899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97d560620cc6c92f14764e562c4cb46e2e8e5cb4ebe3babc436d36f0d51d012`  
		Last Modified: Wed, 09 Apr 2025 21:19:10 GMT  
		Size: 32.7 MB (32737886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b114c3e175f9b076da8bffa62af3710838682fdda2218a124e75942501d8b90`  
		Last Modified: Thu, 10 Apr 2025 01:51:45 GMT  
		Size: 6.4 MB (6363496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5456a508615445072495e9b8d3e1709d0e9677999e3ebacb66dd8f42c301bad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbad7573a661f88044dc762a02e8756799c863c977667a7001127903033c188`

```dockerfile
```

-	Layers:
	-	`sha256:1121e949fb9190abccf5f4453dfb7b4ff0d99dbe2eea865c4d28eb13a03dcd84`  
		Last Modified: Thu, 10 Apr 2025 01:51:45 GMT  
		Size: 2.7 MB (2700850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c6533767e73839fe96e3e848fd36f704c8530b07b7f257605b6748e5747c850`  
		Last Modified: Thu, 10 Apr 2025 01:51:45 GMT  
		Size: 9.0 KB (8982 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:35c6003e84e67433e1f7ab6d143666fba833868a7d3510b587ef5de22937d1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69509429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb8f03a8c2fe9ed9391647fcc8f59ceb7bc6b93fee4cf623b42758eaa576007`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["pypy3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5d2511fbc40055a5e9c3397d58e3ac4f51bc778fa8fc912f45f5b965130ceb`  
		Last Modified: Wed, 09 Apr 2025 19:05:00 GMT  
		Size: 1.1 MB (1079104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed95b0be78afe610d69e26499e1ee6a806ccf1f86d2d3c9c8bc0d17cdf33b44d`  
		Last Modified: Wed, 09 Apr 2025 19:05:00 GMT  
		Size: 30.9 MB (30882378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dddcb932196373102749b23552fdc0f063ca5f8950e48657deba44f030eb18a`  
		Last Modified: Wed, 09 Apr 2025 19:08:06 GMT  
		Size: 6.4 MB (6363374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3b25f25f8af233aefae89f371715d834e908233c0c11aba9a2518c822afc2994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75740601bc0aff1bb38a33bf94a67c458ebba48c2cd21668bdf7901d271647`

```dockerfile
```

-	Layers:
	-	`sha256:0840a78f4212a27e81fbd9cc932d4ef946f9b97292f2c5206429af349c70fde0`  
		Last Modified: Wed, 09 Apr 2025 19:08:06 GMT  
		Size: 2.7 MB (2697655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:763bf06926853f9d80c4831b7cebf413b0149be088c98d0782db80c2940ca3e4`  
		Last Modified: Wed, 09 Apr 2025 19:08:06 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json
