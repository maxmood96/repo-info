## `hylang:1-pypy-bookworm`

```console
$ docker pull hylang@sha256:d398b4bb4d81a2b1de52282464c65f6707e8e5a7d1be05fbf0b00aaad9484f9b
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
$ docker pull hylang@sha256:ff63b7adb19dca579e4a31dd64d278e1febaf6e5f1d8f3e9f08f4fd1da6c608a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76407403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b962486a8f5ce414d08df9d2bc794454082e3cf3834ca7a06f652e108c19f10a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:14:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:15:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:15:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:15:03 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 02:15:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 02:15:03 GMT
CMD ["pypy3"]
# Tue, 07 Apr 2026 03:19:20 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 03:19:20 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 03:19:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 03:19:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e59c0a1f126a93775f573e0c11d73a62865298f65d3918c3f49437f26778e5`  
		Last Modified: Tue, 07 Apr 2026 02:15:15 GMT  
		Size: 3.5 MB (3510246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ccbc9a3462fd9f2591595234d8333a96fd0ffa998dd488e20fc913edcc424`  
		Last Modified: Tue, 07 Apr 2026 02:15:16 GMT  
		Size: 37.5 MB (37480094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18379ad4926b87219a853164b0a3ec5f6e50e98a06396504e6721511834a3eeb`  
		Last Modified: Tue, 07 Apr 2026 03:19:27 GMT  
		Size: 7.2 MB (7180731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8c3d815dfa78dbc5162d9ef5cd17e277dbee523d565b417c83b2b5b2502512d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab3efd34ba984a8d7b3ca87f46859b76fc5798806dcfdbfd061d9119aedd1af`

```dockerfile
```

-	Layers:
	-	`sha256:3ec3fb1c80598d669f93ca4852ac0790b80cd4a5d467cad25372dc279bcb491e`  
		Last Modified: Tue, 07 Apr 2026 03:19:27 GMT  
		Size: 2.7 MB (2683531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e732f76ff0bdce0ea7d9f87fe27bc6a586c3341052b47d22989ff0edd3128d06`  
		Last Modified: Tue, 07 Apr 2026 03:19:27 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:46f9c647d96216b87794d719a2684cd37ebe74b04a5a19a9501a619483967364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74372683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b1c0ff5cdd8f1990e424c71ea588e5e8d8c09eb445c7c217edbbaef2b14307`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:59:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:00:18 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:00:18 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:00:18 GMT
ENV PYPY_VERSION=7.3.21
# Wed, 22 Apr 2026 02:00:18 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 22 Apr 2026 02:00:18 GMT
CMD ["pypy3"]
# Wed, 22 Apr 2026 02:48:16 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 02:48:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 02:48:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 02:48:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea5b17c7d3e52e0bd1e87de6e56fc0a1ac5bf1064c2c2a3a45459b56d90127`  
		Last Modified: Wed, 22 Apr 2026 02:00:31 GMT  
		Size: 3.3 MB (3343236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2c1e6c2277ae89ad94b684c4a542a71090ca171d0165336bb4a89683b97a8`  
		Last Modified: Wed, 22 Apr 2026 02:00:35 GMT  
		Size: 35.7 MB (35711460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f59236aca2f3562b31dfe4544f6346972baf06ce90ac8fdfdb7243592ee30a`  
		Last Modified: Wed, 22 Apr 2026 02:48:25 GMT  
		Size: 7.2 MB (7201873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:47921f03aaa1fab851adea7b61a3c7a06a3b454b4e40c74ba199abbe158cc638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e947e49dbb1ed1dded0699b451e71f504632e01066640e1c7a20441c6c6780c`

```dockerfile
```

-	Layers:
	-	`sha256:59a93be585f4bffac901f48b5305ba1b6e4cfc537ba6ad798e1ea639731e71ef`  
		Last Modified: Wed, 22 Apr 2026 02:48:25 GMT  
		Size: 2.7 MB (2683850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fce6ae6bde2a8b588b5ecace64b80964ffe2610914c405ccacf5d52d34d48b`  
		Last Modified: Wed, 22 Apr 2026 02:48:25 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:0f3174fc40e6f28840b0130e21e3bd29597dbc2c4ebdb8b0588df4f85db06b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73825420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384f7fc3ce92e59fa140e3da78e895ab5f32522ca6e45020c08a5b91360bd058`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:56:52 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:56:52 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:56:52 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 01:56:52 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 01:56:52 GMT
CMD ["pypy3"]
# Tue, 07 Apr 2026 02:57:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 02:57:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 02:57:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 02:57:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220ee4758595ad8d93fef5380284836052acd771811bfe3e413060a3e65ea5ed`  
		Last Modified: Tue, 07 Apr 2026 01:57:02 GMT  
		Size: 3.5 MB (3512886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce439366dc4ed10b8f11f9d5ba6e559909884af5e1b306fe58045bb38a1c88`  
		Last Modified: Tue, 07 Apr 2026 01:57:03 GMT  
		Size: 33.9 MB (33910258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017b22af7f7921737593c9aeeb6a3d588fda02254b5159a0e028d02364be74c`  
		Last Modified: Tue, 07 Apr 2026 02:57:11 GMT  
		Size: 7.2 MB (7180508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3ae8c1329e3451707bf831e351733e5c50f7416bb521a68ad7ba3277cde5fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912fc87b8091feb0ea88ca78a2bb3250435d7ca22b67ef4c58833e854dcaec24`

```dockerfile
```

-	Layers:
	-	`sha256:cf7e2ca27db427b077c5448d6c27d4dad94b664e079a02eaa3a999f80ef0c67b`  
		Last Modified: Tue, 07 Apr 2026 02:57:11 GMT  
		Size: 2.7 MB (2680666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839d5db123483dba711659a251a8ce4680b183e09bb0193e4a909cd2245edef4`  
		Last Modified: Tue, 07 Apr 2026 02:57:11 GMT  
		Size: 8.8 KB (8848 bytes)  
		MIME: application/vnd.in-toto+json
