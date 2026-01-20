## `hylang:1-pypy-bookworm`

```console
$ docker pull hylang@sha256:7dd63b85fcd4fc2eea7b9dce9dd005192f8e6889736fb01303530a1567886b77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:460c3739d0367ab1e3503fe9d8a2bf0284c93503d0ed52191c7ec6d3e3aa4ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77762610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec2c242acb70b5b2a078a6aa13c6c102f31af00027dcf4aff2d828de32bcafc`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:02:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:02:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:02:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:02:33 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 03:02:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 13 Jan 2026 03:02:33 GMT
CMD ["pypy3"]
# Wed, 14 Jan 2026 22:01:06 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:01:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:01:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 22:01:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599518da210d88248194120bec07ce6bd047c1c86e51048b8706a59a7f4c09e3`  
		Last Modified: Tue, 13 Jan 2026 03:02:51 GMT  
		Size: 3.5 MB (3509965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb21a61706e02ba9abc36101b51320335260939f03c91342909abc103f484f74`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 38.2 MB (38206983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85b4e73b0c38e3f38c2d52e78c78faf7a55fcdbf6d988921263e9da4f277c6`  
		Last Modified: Wed, 14 Jan 2026 22:01:24 GMT  
		Size: 7.8 MB (7817090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b382da3482dc8dba7fe36bc8a6d07f594daf24f0b49fbcca61b20fabf4834560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b60a1ac37aae724c022374500d0d2d07395da671d81da902b20160b6ce94dc`

```dockerfile
```

-	Layers:
	-	`sha256:3cf23073c8cbf853658d1f41c880f535e40066b0824728022e809c44356470a5`  
		Last Modified: Thu, 15 Jan 2026 00:19:27 GMT  
		Size: 2.6 MB (2618905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864a38fa72c5011a1dee9e3dd643b98b5650150098dd646f4341fdd49085cbfa`  
		Last Modified: Wed, 14 Jan 2026 22:01:15 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:97b5dfbbb005ea4668295cecd5546db9dac79b2498da0bd02b222b0d3ffd3135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75789915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bb28faa9390a41d5479cd815888d472c446ffab2429b4967332ce2bc2523f3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:08:32 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:08:32 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:08:32 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 03:08:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 13 Jan 2026 03:08:32 GMT
CMD ["pypy3"]
# Wed, 14 Jan 2026 22:01:11 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:01:11 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:01:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 22:01:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42853a26e2a564eeb95a1617ace937ffe3718264e0a06435fab4a21cece8af3f`  
		Last Modified: Tue, 13 Jan 2026 03:08:49 GMT  
		Size: 3.3 MB (3341726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c8196418063e859e09dd1554701e05a0e7110fa367cd8b57d628d545c98b`  
		Last Modified: Tue, 13 Jan 2026 03:08:52 GMT  
		Size: 36.5 MB (36523281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29835f50b0679f6842b7c729ff649ead91578e7ed5d5287adfc570f4c4c2a2c1`  
		Last Modified: Wed, 14 Jan 2026 22:01:19 GMT  
		Size: 7.8 MB (7817019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fb6d2b25bb17670336d785b83793f6999ae6b20bd414c3398836ca6bf15d9062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4086d78098172d451fb052d5588d498b06488a492d1266399379fe95f55a7a`

```dockerfile
```

-	Layers:
	-	`sha256:d41000834672ade78034e43a83fa942fa359fa612bff1356e075b76bae8344b1`  
		Last Modified: Thu, 15 Jan 2026 00:19:32 GMT  
		Size: 2.6 MB (2619220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b738f67b8cbdc9d0b9e8fb28773003f715ee944768f35fc1c85785d42440728b`  
		Last Modified: Wed, 14 Jan 2026 22:01:19 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:3cc457988a24e908212e4e1145ef26c5626300bbf58539ef9e07848d2a1577be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75238478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1230a9b14c59fe966d20a9bdd4a157fe4a278fbc0e6aee5792c2944d9d5c2a6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:30:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:31:21 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:31:21 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 02:31:21 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 13 Jan 2026 02:31:21 GMT
CMD ["pypy3"]
# Wed, 14 Jan 2026 22:01:39 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:01:39 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:01:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 22:01:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1fea3d37ea376adc57699529f79c628e0fb7e89d2b4512248113cc7c2ae23b`  
		Last Modified: Tue, 13 Jan 2026 02:31:37 GMT  
		Size: 3.5 MB (3512237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac579546d54a421e8cb478378344bd8f9f6ea1db2eaf98aa4c63bd6ab7bad23d`  
		Last Modified: Tue, 13 Jan 2026 02:31:32 GMT  
		Size: 34.7 MB (34699347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d5b7234f04a459126784735db7ae6d1044eda992773e663c1be5e2c4c4395`  
		Last Modified: Wed, 14 Jan 2026 22:01:51 GMT  
		Size: 7.8 MB (7816827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:0ff12ed0cd402b9988dfc17a70a739cc640d11dc4ce94a1dfc7fb884a520112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d823030e19beda748c7f7b5d9e0f3e1a45666a21907a86de5e2028ce1f3cdb1`

```dockerfile
```

-	Layers:
	-	`sha256:77ec0b6b2aad9d01d5ffe271a2b5bb98b4cae8047955fcd450824c7288c9078b`  
		Last Modified: Thu, 15 Jan 2026 00:20:08 GMT  
		Size: 2.6 MB (2616048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f889b0eac034b3420ef8c70874b5619a37bfa78358e19ac77ff57b42f6c3eca1`  
		Last Modified: Thu, 15 Jan 2026 00:20:09 GMT  
		Size: 8.8 KB (8848 bytes)  
		MIME: application/vnd.in-toto+json
