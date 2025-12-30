## `pypy:2-7-slim`

```console
$ docker pull pypy@sha256:69955a6f355577319d8cec7217f9202e9ab109e8c5d180782deabecdb50064b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim` - linux; amd64

```console
$ docker pull pypy@sha256:1676389f67a1df9ac15f4ffb788635bdb1c9679e257f5639f0e0ca50a9e61aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65441507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76e96efb2a2393262b1c852fd5250ad44d473f566b962bb8a86c648bfa96aa6`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:31:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:31:54 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:31:54 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:31:54 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 30 Dec 2025 00:31:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 30 Dec 2025 00:31:54 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0f0fbe48ed7b0a5d7f4da02e6297e289b0884edf134334f75bab40c7071573`  
		Last Modified: Tue, 30 Dec 2025 00:32:10 GMT  
		Size: 1.2 MB (1220095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f7fad7c8f0a252e6d5cd04093e5baf8a96198da5d9cc6f307d432a66995ef5`  
		Last Modified: Tue, 30 Dec 2025 00:32:12 GMT  
		Size: 34.4 MB (34444879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:ce3dc534b5d5c4cc8cb72b289481d933118f3d918544dcb88568be8f850a7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d914feabfc3fa0b5e6215212901f029a96359c236e2c4546a6108f3cd7548611`

```dockerfile
```

-	Layers:
	-	`sha256:a0deb7b06c3678a31f41e87e31f8970bbe9178112d48932d38550f625c0d2e93`  
		Last Modified: Tue, 30 Dec 2025 01:39:42 GMT  
		Size: 2.1 MB (2131842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3aa61d8d44839d049f3c4c68a32c38db9a5bcdc3b1429973a0b78874fa9674`  
		Last Modified: Tue, 30 Dec 2025 01:39:43 GMT  
		Size: 21.2 KB (21215 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:dcbbaa27b34862b0c4cd5a8173b32998488378bdb8157b60879bd00f2498ca02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63697340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3863b93060135e59f22dd849098604d9cd5900acdc43618c1c7d24436cdcc52f`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:33:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:33:28 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:33:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:33:28 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 30 Dec 2025 00:33:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 30 Dec 2025 00:33:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b232abb0cfa7ebe72eae9ed223d440c07a373227eeebf9242318aa536e7869b`  
		Last Modified: Tue, 30 Dec 2025 00:33:45 GMT  
		Size: 1.2 MB (1202340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b4392856db1e92750f9ae8df65978fdc16032a8436e10094a143b420f2a97`  
		Last Modified: Tue, 30 Dec 2025 00:33:57 GMT  
		Size: 32.4 MB (32356364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:ca5c640321a99d62f5f67c36ddbc7866875b92b9ed4eff151a0abe6c6dea342a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd68ffbbdc954480ec88a675858f2bb344cac8f6807fae98a037c55fc0a53e7`

```dockerfile
```

-	Layers:
	-	`sha256:8c97182f2ba71cb340537fc1b8a26467d4da558abbf91319cb590b701f7c12ab`  
		Last Modified: Tue, 30 Dec 2025 01:40:03 GMT  
		Size: 2.1 MB (2132249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c976e97b54be8e87778ac67bb2dd3b3a0576e08c8d84c2611ab1fc522d4834`  
		Last Modified: Tue, 30 Dec 2025 01:40:04 GMT  
		Size: 21.5 KB (21477 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim` - linux; 386

```console
$ docker pull pypy@sha256:13d2f7adc96b158c4a45e39bae2b7e958e4e3965b249bfcbc864348fde66c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62520333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf749e20b998e5d6df6c25ccb761ca1794012130ccbfdc20eb346b88847a4b4c`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:58:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:58:29 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:58:29 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:29 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 29 Dec 2025 23:58:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 29 Dec 2025 23:58:29 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa909fc559fb3f89eb3be147341a92f6bddbe7f1571f1703a3786c01ff64efb`  
		Last Modified: Mon, 29 Dec 2025 23:58:45 GMT  
		Size: 1.2 MB (1227776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8674470877a10f7454553a21570396c146c3e27a10eb78511e34307a9231df`  
		Last Modified: Mon, 29 Dec 2025 23:58:53 GMT  
		Size: 30.0 MB (29999457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:f0986762030b4a6a93eee94f53707894cdc9a92acec40a2d879c95284454f13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e844a87e2cba06964e8e8ba7c52989965e1be1a073a72ad5cfff83beb3df1b16`

```dockerfile
```

-	Layers:
	-	`sha256:98df362c4d9c4de09d1c03eeeb2e0dd10734be0bd5f9938e1c4d09dff9f193a6`  
		Last Modified: Tue, 30 Dec 2025 04:39:17 GMT  
		Size: 2.1 MB (2128969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c9ff0c6a0ee3d113f0be8096ce03c5f8044bfc9aa1caad51b89c0c612dc982`  
		Last Modified: Tue, 30 Dec 2025 04:39:18 GMT  
		Size: 21.1 KB (21121 bytes)  
		MIME: application/vnd.in-toto+json
