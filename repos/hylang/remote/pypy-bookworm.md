## `hylang:pypy-bookworm`

```console
$ docker pull hylang@sha256:c373d5ee3675210b150ab8192dac100155e7bb147c9948d9e12d5251bae522ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:8c8199a986f706a766e629269d093ea7bf2d964aea84d4f953f05eb16fd8719c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77176334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f51fbe8bf3a5f80b8a46fc04bc9821333bfbb302744381b5d7004b76b23a25`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Tue, 28 Apr 2026 23:34:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:16 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:16 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:16 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:35:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 28 Apr 2026 23:35:16 GMT
CMD ["pypy3"]
# Wed, 29 Apr 2026 00:10:50 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:10:50 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:10:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 29 Apr 2026 00:10:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff5dac9962f3b5ef67b2adea4a355f57a3c39b446ff827213cfb8339bbfd763`  
		Last Modified: Tue, 28 Apr 2026 23:35:28 GMT  
		Size: 3.5 MB (3510959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ebc54fb932afa166c4f6caba024fd72bd400b0c06908bb46423b6f41a4f151`  
		Last Modified: Tue, 28 Apr 2026 23:35:29 GMT  
		Size: 38.2 MB (38187729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42df54d426177a509491f7388a1b4751f1d09141b9d65d6c29c10b7da4ea23c`  
		Last Modified: Wed, 29 Apr 2026 00:10:58 GMT  
		Size: 7.2 MB (7241394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:6939b73710eac252c79053298d6b4874263e6eb2af58381c0006ec55a2c2a1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2713117268750a9a2af7abf996296b314bcbf6c29a74df73014c5e4d3ec06c04`

```dockerfile
```

-	Layers:
	-	`sha256:8c266fdb508f24d0a6e131fe0d60a6c32442f0eb6ba2b312b3f55cf7c602b4fa`  
		Last Modified: Wed, 29 Apr 2026 00:10:58 GMT  
		Size: 2.7 MB (2683531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c194dff445b688c8b448418f66ee61b513dfd21099fb2d87d97a4933ed14647`  
		Last Modified: Wed, 29 Apr 2026 00:10:58 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d356ba844a785ce4763aab532cfb10ff7ccd40653468bcba224524f123f73203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75067220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e29265d85c82c5e6688884ae922a17300e7b868e51d9e680abc29a59d673b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Tue, 28 Apr 2026 23:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:36:25 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:36:25 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:36:25 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:36:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 28 Apr 2026 23:36:25 GMT
CMD ["pypy3"]
# Wed, 29 Apr 2026 00:10:51 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:10:51 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:10:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 29 Apr 2026 00:10:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35923d0ab14d7f960ef7303f523f8dcf19bddc733896181fa10e63f65766d50e`  
		Last Modified: Tue, 28 Apr 2026 23:36:37 GMT  
		Size: 3.3 MB (3343175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b322dd63a796f8730bc8d0eaa241ea82a73a08588588f2195246b0d80b2a2a1`  
		Last Modified: Tue, 28 Apr 2026 23:36:38 GMT  
		Size: 36.4 MB (36366400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02a6e0ee58ce96bab7b74000ded278b90ceb242b511f4be55f84781aff89ae`  
		Last Modified: Wed, 29 Apr 2026 00:11:00 GMT  
		Size: 7.2 MB (7241531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:37a08d0f75df311984453f4d140a7f30d0fefed5ac6f8e6a8325f09fa86f1893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02d285e30e64ec40d8cfcf50b28cb2a9df8acfdfa3d9636bab698df1b0e87c5`

```dockerfile
```

-	Layers:
	-	`sha256:0be2a66a8b77baa4c9083146a6283d65ead49cdd0f72bf7b7b7a7417d109d167`  
		Last Modified: Wed, 29 Apr 2026 00:11:00 GMT  
		Size: 2.7 MB (2683850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c344dd02a0acb06220e4c128fa74e90012621ed74631afc4a63cf5bb682540f9`  
		Last Modified: Wed, 29 Apr 2026 00:10:59 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:dd500c0782afd29e97c9b3d3a4134821827f33b12ea0a5e62148c42dd067c07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74298547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4f3cbfa7a52d57cac415452050b6395457619e660a85beffa2c336dbf80cc8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 00:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 00:31:20 GMT
ENV LANG=C.UTF-8
# Wed, 29 Apr 2026 00:31:20 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 00:31:20 GMT
ENV PYPY_VERSION=7.3.22
# Wed, 29 Apr 2026 00:31:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 29 Apr 2026 00:31:20 GMT
CMD ["pypy3"]
# Wed, 29 Apr 2026 03:34:15 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 03:34:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 03:34:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 29 Apr 2026 03:34:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5c450c49853efe285f6caa47a76a4bb037e168526936db1b3a97fcb1a1bbfb`  
		Last Modified: Wed, 29 Apr 2026 00:31:30 GMT  
		Size: 3.5 MB (3514172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f27bcd2a4f9f6573d70162c38ce82bd39f6dfa8eac06ac10649c134d1aa7c`  
		Last Modified: Wed, 29 Apr 2026 00:31:31 GMT  
		Size: 34.3 MB (34321195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2991bebbe1b645e8417eb6f9fcfb4b21c7e5f041360e9dc0a77148a39ae29dd9`  
		Last Modified: Wed, 29 Apr 2026 03:34:23 GMT  
		Size: 7.2 MB (7241484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:6b56652d0bbb5e8089c06a5dbf058cde15d008044a897a1a2b913b4bd5f66704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda8bfc570ec79751db61f4d82f6c5152e38ba25fd0db7b1b60447395cff1ca0`

```dockerfile
```

-	Layers:
	-	`sha256:6a7a10890a690a58af8ea6d0a8a45876570518084ecee74b0defe24b3bd1f547`  
		Last Modified: Wed, 29 Apr 2026 03:34:23 GMT  
		Size: 2.7 MB (2680666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e42790484409ce8a60af5352b0b1b5dd3f8ab83612c736be83d6fb8afce8087`  
		Last Modified: Wed, 29 Apr 2026 03:34:23 GMT  
		Size: 8.8 KB (8848 bytes)  
		MIME: application/vnd.in-toto+json
