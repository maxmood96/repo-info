## `hylang:pypy3.11`

```console
$ docker pull hylang@sha256:92301776a97cd0cd03175fc06e9d7ffa0669262b3b4ce35429ea41c9166e901b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `hylang:pypy3.11` - linux; amd64

```console
$ docker pull hylang@sha256:cd0fd637a13708187f056bd5bcb2b44a871b97f584175a19dd75940b246efabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76702946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383370e003e752ae271f95efe0da14ded01d380f0725d4076273df937a53cd30`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:29:15 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:29:15 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:29:15 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 08 Dec 2025 23:29:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 08 Dec 2025 23:29:15 GMT
CMD ["pypy3"]
# Tue, 09 Dec 2025 00:59:23 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:59:23 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:59:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:59:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde73e7277122c61c5f9c2f17d30f2c1333e1b9634964325ee8121a024ead0c3`  
		Last Modified: Mon, 08 Dec 2025 23:29:34 GMT  
		Size: 1.2 MB (1220164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f7125b3dd1b9527698962bb3512e1285e4f734a80e57b1ebd2718f87cb539e`  
		Last Modified: Mon, 08 Dec 2025 23:29:36 GMT  
		Size: 37.8 MB (37838752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efcea573ed1f5c7473dd4ea43b62241e2f23ee494836da5e4227b5012fb06fe`  
		Last Modified: Tue, 09 Dec 2025 00:59:37 GMT  
		Size: 7.9 MB (7867534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:bc9fd41a0e27734b2c2bc302694b6083a81c087935cca1b3fe8cde134b3ea502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fa6b86e4a840fe1e30253b255975d49a8f9c3905fb1b68fd08f92034b4b2f8`

```dockerfile
```

-	Layers:
	-	`sha256:81c35a77e29eae12cacb27078066dba64a8b3337dd39ab81e0844fa8abdf6e9c`  
		Last Modified: Tue, 09 Dec 2025 03:19:17 GMT  
		Size: 2.2 MB (2238806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f8e60ea57e06144f47499378bf81c305b64306e6964193e27723e3874b5e4e`  
		Last Modified: Tue, 09 Dec 2025 03:19:18 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5e4810be4a5afd4c857c1f60566fbf7c3f74603c6e7938a2c336fba3e9d2e6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75365015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40939ad1648fc97a5a06b7799112a27bbb7d0f30abf6f6f2b3c64cfdab26a36`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:30:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:31:13 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:31:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:31:13 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 08 Dec 2025 23:31:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 08 Dec 2025 23:31:13 GMT
CMD ["pypy3"]
# Tue, 09 Dec 2025 00:57:01 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:57:01 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:57:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:57:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c7beb6eb1a2025e871e881adb7b106be29751b9148ba410b74fed8aba5cff6`  
		Last Modified: Mon, 08 Dec 2025 23:31:31 GMT  
		Size: 1.2 MB (1202325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555811bf98367027c3536125d4700c3f014d37a010fae3b8c29affeaeab65773`  
		Last Modified: Mon, 08 Dec 2025 23:31:34 GMT  
		Size: 36.2 MB (36156407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fd9f708d5d4355451964b78d37038118912a9c56d9ae11b549caf2823402c8`  
		Last Modified: Tue, 09 Dec 2025 00:57:15 GMT  
		Size: 7.9 MB (7867655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:306fa32669009db00c84b0c3c20462ac5983794cc1da5edca2985a0757e0050c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a867d50e77f8acbea2c868be0c2b44761f99b49c9b5c6aed9b6a544076418276`

```dockerfile
```

-	Layers:
	-	`sha256:01869aa938af5021059acf5abd89564e8e538a2fe90576cfd88b4a6b8dbc9fed`  
		Last Modified: Tue, 09 Dec 2025 03:19:22 GMT  
		Size: 2.2 MB (2239217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f3866a906bce377881cef66caa679ea84e90a9f534325ec3b3965f52089ee0`  
		Last Modified: Tue, 09 Dec 2025 03:19:23 GMT  
		Size: 11.5 KB (11536 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:2b27a78fe970d712ee9eb4105aec270c0f2d1b50943acd306b9ee0265b60719d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74625350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75460293d6c7d847d2671b3b90e7a2ab26577bfe0f2f858ac876c8c3ab44e85`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:23:36 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:23:36 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:23:36 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 08 Dec 2025 23:23:36 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 08 Dec 2025 23:23:36 GMT
CMD ["pypy3"]
# Tue, 09 Dec 2025 00:30:16 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:30:16 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:30:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:30:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071ae2effab28d1d56db48b7f236437a9cf0aa635b0c26e3198a9b1fabb31307`  
		Last Modified: Mon, 08 Dec 2025 23:23:52 GMT  
		Size: 1.2 MB (1227761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2988de35c77d31fd2433ff3f1d172810c03a11989c8ea879f513de6284a87f13`  
		Last Modified: Mon, 08 Dec 2025 23:23:54 GMT  
		Size: 34.2 MB (34237039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecfcd21c5f946a2884deebc004eb1785da49d27d355b7ed5b8d8a608f2b561`  
		Last Modified: Tue, 09 Dec 2025 00:30:29 GMT  
		Size: 7.9 MB (7867480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:033568dd4cb1c30c8d2dd586435b91baf4aaabf07ae25db34f2eaaa7d3f7cc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0830f33898cb59ab457ed6db754dd317d1d8a4b88a27e4cf8b968ca26acb752`

```dockerfile
```

-	Layers:
	-	`sha256:1f98063db58820b627af26f1fc9cac47284d1ff2f9a3bfcc2780444c270c68ac`  
		Last Modified: Tue, 09 Dec 2025 03:19:29 GMT  
		Size: 2.2 MB (2235925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdaaeae68bb2ee8e535455ad50c1d17a78579f92d3e14915d82e8fc73d75300`  
		Last Modified: Tue, 09 Dec 2025 03:19:30 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:2117ef1239da2e8e10bc068251d78a0b181446d24274c277e8c4f5b69da3c0a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290863173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bc71b90ea4ba0f084a9903e063d35667844706c41778542f27d0ffe0529b00`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:27:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:27:23 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:27:23 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 11 Nov 2025 19:28:06 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:07 GMT
CMD ["pypy"]
# Thu, 20 Nov 2025 19:44:30 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:31 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:30 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:45:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3946b48a3a8e69231ebe93558658226c6e53f281d568fd74b5e2fda8d16fc17`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 358.9 KB (358917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ce9f865a1fbb63ea6ed95fd2f3ea88bbf38551e91515451f0636e5b698aae1`  
		Last Modified: Tue, 11 Nov 2025 19:28:25 GMT  
		Size: 15.5 MB (15529573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628114af2eda98472aa5ec10fdc837f8ec8a924a4c0306bb2b28686529694cb`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6b8c56e76c031cbd1e553f2eb5d1e8af9cb75b0b1d6046d6c87d0b6daa2c95`  
		Last Modified: Tue, 11 Nov 2025 19:28:27 GMT  
		Size: 30.7 MB (30670943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbf78de2bbdb6d3dd6712af6b8568aa09ef6135c1639945a7e3c8ac78b4739`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51553d7ef7b6784ddc172b974527503ebabc753edc57bf3361523c780584aa5`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f44ddd8e5847c59fe60403e4b67008529261dd26ef36456416f412cb053a04`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea642060bf8e61750450bf45ba4d0ede87d1eda3807058a426b2e0411ab548db`  
		Last Modified: Thu, 20 Nov 2025 19:45:43 GMT  
		Size: 8.8 MB (8840144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84de9dcbad826db5b329fe417c0cbc2bbcc82be7edf6353f2b5b29ca70ec7e2e`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.11` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:df129f6d66851e1c2a1891c8af3744975af058b0769e6d4097289225ed31635c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825488411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de3ae1bceeb233fe69db5c032d1690a72765a0a90ab61847d9270042ab9e382`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:24 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:25 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 11 Nov 2025 19:29:03 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:29:03 GMT
CMD ["pypy"]
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:43:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d80c29a0842a34f8c512d7c99d3ec6a50bc0da8baa6234281af26593606c756`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 487.9 KB (487935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c736ff67c1729815898cab1f0ce89d5cc7b38c9928a3fea417d6ad98d67de66`  
		Last Modified: Tue, 11 Nov 2025 19:29:22 GMT  
		Size: 15.5 MB (15529843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3ced131808af1789c74f41256a2ab4d8e46d6013f7e28cfdb0bb2633dc4b8f`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9685518121426f07f379bea6b65794018f09c0c737b442db076d9db44acc80c1`  
		Last Modified: Tue, 11 Nov 2025 19:29:25 GMT  
		Size: 30.7 MB (30672291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea916fe33d8d87609385929be1936f8ca3934e23cec287a7b788a7fc5badf25`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a788febd4647e53bca83411bacc17e560fbd0e54ed9b76a66879585bf81c30da`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a675be48786f954763d72d3a128348086b736ba6950c7385816eac1388858a2c`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde02c42db77134fc27b0ba615febed876dbc24b01f8c36f50c5dc0af14eda9e`  
		Last Modified: Thu, 20 Nov 2025 19:43:41 GMT  
		Size: 8.8 MB (8829029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2be63de21791d6f9c102c011e9fe8497ee4e74fa5db9710254ed31a90cddd40`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
