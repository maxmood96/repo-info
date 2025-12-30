## `hylang:1-pypy3.11-bookworm`

```console
$ docker pull hylang@sha256:779458f244b302b39be0c6da4ea972708cc85526934e9395b4a38bac3c05dadd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy3.11-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:d7723588fec64300b64c09f745d615b2c1c71381fcf27199fb11cc919a4df208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77812295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3c6105f7ecd4256e8231409951d8764aa47141c00b4ee8259c36ed43bf996a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:32:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:32:03 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 30 Dec 2025 00:32:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 30 Dec 2025 00:32:03 GMT
CMD ["pypy3"]
# Tue, 30 Dec 2025 01:52:00 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:52:00 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:52:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:52:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4aefe667f4b5b7a7debbae3c16ecca50ee8baf62f0822afcb383588f074ea7`  
		Last Modified: Tue, 30 Dec 2025 00:32:22 GMT  
		Size: 3.5 MB (3509686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefbde2327349791aa82d557a278903dee741e9f514e1445c6e3838ee50e9161`  
		Last Modified: Tue, 30 Dec 2025 00:32:25 GMT  
		Size: 38.2 MB (38206803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e363bad1780335457814b74bdad697a601c9028479552bc6eb9dac400f3852`  
		Last Modified: Tue, 30 Dec 2025 01:52:13 GMT  
		Size: 7.9 MB (7867382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:995adf0d8d6d06391564e56a61af37c91348c0fdb2cc0bab7df87aa46d6b5a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6febad84356c447ff322464286210561cbb720a90fe9a38c52b11830d343cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:26adaace881798693b2c1ed3d83755c9ba3eced18c8d50084028d4590aa13b3d`  
		Last Modified: Tue, 30 Dec 2025 03:24:13 GMT  
		Size: 2.6 MB (2618895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c22784b03e209444a3a1f2a3fc76aa621e798955ae36561b41e8e1a72fa6fb0`  
		Last Modified: Tue, 30 Dec 2025 03:24:14 GMT  
		Size: 8.9 KB (8898 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9f33b04dab787b1443fc0c2798ff9efdd0c8725a94f816bfbe6c12343ee74adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75833682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bded30e79bcccecde066d60315578cbfbbd02ffd6a4d4210456d42e379199b8`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:33:45 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:33:45 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 30 Dec 2025 00:33:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 30 Dec 2025 00:33:45 GMT
CMD ["pypy3"]
# Tue, 30 Dec 2025 01:51:37 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:51:37 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:51:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:51:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4eb94d70d264267c4801f17cceae25fab3ff1f9fef2f7118105883c73c7730`  
		Last Modified: Tue, 30 Dec 2025 00:34:03 GMT  
		Size: 3.3 MB (3340654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defa6ed9260371cdb8c0e4a54649cf56e438ba758095e73aa79b19ff150ccdbc`  
		Last Modified: Tue, 30 Dec 2025 00:34:06 GMT  
		Size: 36.5 MB (36523227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c728d35612f2e83fb14d5d89a83567141e7fe329a14bbc40757b111c19fb6335`  
		Last Modified: Tue, 30 Dec 2025 01:51:50 GMT  
		Size: 7.9 MB (7867591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2025305824d54433d8195c2d1400fb740baf6858779ab103b0bc943fa7e2d6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a2585f2eda9aa6a1fdcc43afe630a53a80c7d247f4869f0c9b5e17462c7e14`

```dockerfile
```

-	Layers:
	-	`sha256:7d47f9903417670913bf16a169a794eac131241154dfa7d8bfbd704d195bba8c`  
		Last Modified: Tue, 30 Dec 2025 03:24:19 GMT  
		Size: 2.6 MB (2619210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033300f575cd89c5551a82f81aa94d0a70510fca759573040d970be901027d48`  
		Last Modified: Tue, 30 Dec 2025 03:24:19 GMT  
		Size: 9.1 KB (9051 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:7eed6028537ea60fd916293f0d42d8bd6409c3e44b92d49a02a2272b789e9b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75287570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c467dd7adcf4cf55744ccfed8fa6a926452ec47b4dc3827377aaf473762038`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:58:04 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:58:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:04 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 29 Dec 2025 23:58:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 29 Dec 2025 23:58:04 GMT
CMD ["pypy3"]
# Tue, 30 Dec 2025 01:09:52 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:09:52 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:09:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:09:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdc3f39196e26fa487313e555f78a561ecf41b8a252002acd0c3692fc4da707`  
		Last Modified: Mon, 29 Dec 2025 23:58:21 GMT  
		Size: 3.5 MB (3511012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10d32553254a598e4d6fc5e93e7616486ab0dac2a65da5fd18f2573904b1aa`  
		Last Modified: Mon, 29 Dec 2025 23:58:24 GMT  
		Size: 34.7 MB (34699315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5700dc3abacfa8c9e800bad4fe6c23c5b89aafc5312c7aa61ebadee3d013e06`  
		Last Modified: Tue, 30 Dec 2025 01:10:05 GMT  
		Size: 7.9 MB (7867470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:03e906aa9e19b415d891a3c278aea50d77c92ac0adff686696c9fa0b8bce7bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5504c76453e932c45fa3931030386c844124b046d3f8bd28181150f770d01da9`

```dockerfile
```

-	Layers:
	-	`sha256:e2e0b95049c08f61afb47da9a8f422ea784fa610c577a69e59377c68d7d1f8c3`  
		Last Modified: Tue, 30 Dec 2025 03:18:45 GMT  
		Size: 2.6 MB (2616038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16036067ca58ba5af20972874db8ce168a42e09f3269d983b84621b7aa298af5`  
		Last Modified: Tue, 30 Dec 2025 03:18:45 GMT  
		Size: 8.8 KB (8848 bytes)  
		MIME: application/vnd.in-toto+json
