## `pypy:2-slim-trixie`

```console
$ docker pull pypy@sha256:276fe6a9faf92e7675f5f2126222687fd45f22ce716af7108eecb0d27905aac7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-trixie` - linux; amd64

```console
$ docker pull pypy@sha256:859a5c8c389e130c2534a1cb101322e961705476039d2f8d4111506a9eec76bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65442372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07219eb7766f6c8f1113d25569474865887efd08dea493b78cb1fff1c74c6346`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 08 Aug 2025 20:00:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5833c5aced7752eeeca9625a76c7cf8d0d7e9c4f153e9bec03d604407e2db04`  
		Last Modified: Tue, 30 Sep 2025 00:32:10 GMT  
		Size: 1.2 MB (1220342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d31e0342efa3a32e6863644bcb9893cac826ac88ee5af41608129eab7feb213`  
		Last Modified: Tue, 30 Sep 2025 00:32:13 GMT  
		Size: 34.4 MB (34444264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:47863d69a79b9608d523ec09763b430a138d740a275b64e5ecfbd70fb072e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3782559be573947014ff7fb287aed6aacfe81d280a249c74131bcee2e759b040`

```dockerfile
```

-	Layers:
	-	`sha256:f924a444a6240ae33c75433044b44b0426ccde23b2088e98bc0684bdd230a6d9`  
		Last Modified: Tue, 30 Sep 2025 21:38:43 GMT  
		Size: 2.1 MB (2131758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7876df1f20f38b8b8f27c10d17da6e51a0e5c320b411957f549b88ebb4049c2d`  
		Last Modified: Tue, 30 Sep 2025 21:38:43 GMT  
		Size: 21.3 KB (21258 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:e2dd7932a2e59318d90d31b50676c8f7ef24287c23074d54478dcd2346053b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81af4a1e587c1f89eea2eac22e1879362746ee01a38fa05093f33d7080b73f28`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 08 Aug 2025 20:00:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfcb5d62720e0ac5c5c8dbae37d5e386f293eeea49f1b09cfd9f216d581a5fb`  
		Last Modified: Tue, 30 Sep 2025 00:32:01 GMT  
		Size: 1.2 MB (1201945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5ec58afd344d4822b2e58683e7702476b5669a6b6988d16a7a1bbc89645209`  
		Last Modified: Tue, 30 Sep 2025 00:32:02 GMT  
		Size: 32.4 MB (32355559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:5f5f2387660bce3d7466fcd0d126cc87c4e1afc885d11b45e3218b9133226f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93e13bbf5f53861929e5faeaafe6ab30f5158485e8086352724f8700c5d39e3`

```dockerfile
```

-	Layers:
	-	`sha256:c048a1307d209f9a449eef25dc2619980ab8869459a73cb0bc5035ecc71e618d`  
		Last Modified: Tue, 30 Sep 2025 12:38:38 GMT  
		Size: 2.1 MB (2132165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7d3d861ad0ac966bd28c3df1a59329b7fd8d7b6fd01bd0751803936f28b59c`  
		Last Modified: Tue, 30 Sep 2025 12:38:39 GMT  
		Size: 21.5 KB (21521 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-trixie` - linux; 386

```console
$ docker pull pypy@sha256:2a5ab36a9f6cbac5b9feb9db2f1f433764148c215cc2b11fda799d51916d69d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62521488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd0eb137d75bcf14977c8bebc3e03707378d9497a99dcc314448ca7cbd149d8`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 08 Aug 2025 20:00:48 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 20:00:48 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 08 Aug 2025 20:00:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 Aug 2025 20:00:48 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e6b4680909527dcff00cc5edb927f26d9b6b5881b531476c4ce437010f86b`  
		Last Modified: Tue, 30 Sep 2025 00:31:09 GMT  
		Size: 1.2 MB (1227870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5620ba4aa5be4d6ab1c5b4ec748155405d1effa35b92c21da8ebc6f437c0b6a4`  
		Last Modified: Tue, 30 Sep 2025 00:31:12 GMT  
		Size: 30.0 MB (29999082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:0031c8cce0f97ddbf1dedae4d316e3f9bf73c9bb040a1a5382c7cf994d9208c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86cb83fc5cd1e44ad0fa0be8f1d43941b1fe882e20521186a384d4cfa71946c`

```dockerfile
```

-	Layers:
	-	`sha256:03ba3ad424bca22bd51b97bee627490f67ca6bab1d6771f5cac7ee0f2e8bcc5e`  
		Last Modified: Tue, 30 Sep 2025 15:38:37 GMT  
		Size: 2.1 MB (2128885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba92556962500cc25f5e7777fdf5730e29e6a9a395e89e49fa766b9cfa67235c`  
		Last Modified: Tue, 30 Sep 2025 15:38:37 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json
