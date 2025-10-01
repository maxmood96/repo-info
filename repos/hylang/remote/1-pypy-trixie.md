## `hylang:1-pypy-trixie`

```console
$ docker pull hylang@sha256:870405a504fb04c2bf65ed29509f4c343fd65b13fc6cf3f85d95139f4fad8a55
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
$ docker pull hylang@sha256:fb564e7838584682806aaf1c611be4a0488321a8c260b0c13cb5e550e537cab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75271794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320d21ad47c0eaea699e599e1c8427ee6c3d273dba3760a8063f1fc624791e95`
-	Default Command: `["hy"]`

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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d6d4d7cc8160b8e685303fcb6f8b8e1585071c6dff81759599e19737a1099e`  
		Last Modified: Tue, 30 Sep 2025 00:32:01 GMT  
		Size: 1.2 MB (1220348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e628d0d33757db57ae1baf9c5368e41e4a194ef43f5593bca494134b7b6268`  
		Last Modified: Tue, 30 Sep 2025 00:32:04 GMT  
		Size: 37.8 MB (37838475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e1918ee374a85b0dabe0cb99029ff41291bd0ed57cb4dea68070a6a99f921a`  
		Last Modified: Tue, 30 Sep 2025 03:37:06 GMT  
		Size: 6.4 MB (6435205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:ed919251de3077213349bf5cf2f36ecb791c513ba58f184e703a984b929dfb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0504fb9c101a15ea6fa9fab05182baddf61ea8e1be2aa636631161b198c1b30b`

```dockerfile
```

-	Layers:
	-	`sha256:40c8d60f22a897b0ce20f314608302fcb80c54b8a36a9388347d313b23d70c69`  
		Last Modified: Wed, 01 Oct 2025 14:17:34 GMT  
		Size: 2.2 MB (2236326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a87af425f68a3e3f52567ad263d5dd5b137d6b9fc226f6382f91ff7a74c9c70`  
		Last Modified: Wed, 01 Oct 2025 14:17:35 GMT  
		Size: 8.8 KB (8793 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:edfa7735b5005bfa6a202ed3186fe2862aa08a2892b4f9b7dfe58020d5608c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73934459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc379118aac71a9663e95f53e39af389c698c4a137c24e5340125db089c78699`
-	Default Command: `["hy"]`

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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe52096b4c1937fdf3f3c4684d16654da105ebdb52ccbbbdd35fe6c79acaa6d7`  
		Last Modified: Tue, 30 Sep 2025 00:32:01 GMT  
		Size: 1.2 MB (1201954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553f2cd40b475eacaceb3ab6413dbb1542271a1b04de4c841a701846255a54ba`  
		Last Modified: Tue, 30 Sep 2025 00:32:27 GMT  
		Size: 36.2 MB (36156454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54e1dcc00e48f0c2f5fa71fcafb1b36809da9118f1207ec9b81b36af3dbce93`  
		Last Modified: Tue, 30 Sep 2025 01:25:30 GMT  
		Size: 6.4 MB (6435209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:3a4f7e02ed22011d6795956a6e90d93c6d4b38ef7d2c540064c2ebc98b49f5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4cc3ae77aa868bb0b42ab8f349128d11617ae7c81e40b91040fc8a092f11aa`

```dockerfile
```

-	Layers:
	-	`sha256:87dc0e10fef58dce82d9ec26b3fd250d307764cf23f64a1272ff660474d63de8`  
		Last Modified: Wed, 01 Oct 2025 11:37:59 GMT  
		Size: 2.2 MB (2236641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f31eeb9103668cfd10eb881226ea8ac9097c3434628c05d7e9ad20d62839d5`  
		Last Modified: Wed, 01 Oct 2025 11:37:59 GMT  
		Size: 8.9 KB (8945 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-trixie` - linux; 386

```console
$ docker pull hylang@sha256:c3f693a2554486405c198bce83b2f6dcfd196a7074e5286c242e3cb44a0aa72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73194024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c52fdc6a8c7ccebf9b5c2da96f38398707b6eac2ecf1b5ca7cf03ad062cb8f3`
-	Default Command: `["hy"]`

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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826a58a62d4dbc4ad4fc62f8231ac55842dd44e8e6d2a8c1910781999fc4724`  
		Last Modified: Tue, 30 Sep 2025 00:31:02 GMT  
		Size: 1.2 MB (1227846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcadc30cb22e79620c84f3e78945d684000eb6b1f00d7fa12c086ee68888c5d9`  
		Last Modified: Tue, 30 Sep 2025 00:31:04 GMT  
		Size: 34.2 MB (34236569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ec2707dc3320a0f17832704ac505ce27c717052dd499aacc2895d479753ba`  
		Last Modified: Tue, 30 Sep 2025 01:24:34 GMT  
		Size: 6.4 MB (6435073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8a724e5de7c492e86b745ed828a5cea18fa62b2ab1f3e3d3e4e765ba4730d153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b412f855c8b29d3b635c44e838d6d53b210e5b48f01077bc19b0065c76fbaf8a`

```dockerfile
```

-	Layers:
	-	`sha256:d1ba6df57a22932fd8d49a8521de3a19fc7957e85c76d2c746ab147258688ef8`  
		Last Modified: Wed, 01 Oct 2025 17:25:15 GMT  
		Size: 2.2 MB (2233485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977309456da3c7a8f56d1df8890231845de4a604d13e1a35ac2cd1566e79c3a9`  
		Last Modified: Wed, 01 Oct 2025 17:25:16 GMT  
		Size: 8.7 KB (8741 bytes)  
		MIME: application/vnd.in-toto+json
