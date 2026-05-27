## `hylang:pypy`

```console
$ docker pull hylang@sha256:3422bf1a0b4d7cec3320860cbc73c91d58c015db360faff0c173ac457f228dcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `hylang:pypy` - linux; amd64

```console
$ docker pull hylang@sha256:09a3053dff194a8cf08b082ca0c9633b218876c5154a99297ce76150278abafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76025514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9449d515382ddb7d401ca383adf6b22867f343a2c0e0c013c5203dfffa804ae`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:38:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:39:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:39:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:39:34 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:39:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:39:34 GMT
CMD ["pypy3"]
# Wed, 27 May 2026 00:12:26 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:26 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0e4c1fd3e42f6fb48ea0bdf3d2c5a9e4309612de12e6f1e7813db50dadc9e2`  
		Last Modified: Tue, 19 May 2026 23:39:46 GMT  
		Size: 1.2 MB (1220980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f344c81e7231fc8ad8ec18028961679aaee4f9e223cd243ffc9ce52f10de52`  
		Last Modified: Tue, 19 May 2026 23:39:47 GMT  
		Size: 37.8 MB (37772769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793ee7e93f36d314dc9f98b8e077f62a9c42014e824a5ed6e96bd532cca7d247`  
		Last Modified: Wed, 27 May 2026 00:12:33 GMT  
		Size: 7.3 MB (7251839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:0e5e47c8c61bd6bfe8785026292feb918850de3691006f90239db3a663f93b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e5b81808502977ec5539c532a4f18d7a2482df9eba7b959f8b32d9408ee1f8`

```dockerfile
```

-	Layers:
	-	`sha256:08e8867c008d76e3cf98a2b534e13adc1bbb9188fdc3039b63bb9c8309bb4fa3`  
		Last Modified: Wed, 27 May 2026 00:12:33 GMT  
		Size: 2.3 MB (2297679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162d7c7a75ab3d6292aa0a2f999b044160d1d53ff053c6d92bc1b89f341e3fd3`  
		Last Modified: Wed, 27 May 2026 00:12:33 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1f6b4437e3e826d2ca4614448f9a5ce7a5bed8695f875ece481cec750c440611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74554613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871b1e80823c84a1f1cc1f004889b0dab7a4e9f6493268d2aa43802bc4fefe0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:42:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:43:47 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:47 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:43:47 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:43:47 GMT
CMD ["pypy3"]
# Wed, 27 May 2026 00:12:19 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:19 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8b24f1e4bc7326cf6fd12a2310357886272b080648c8a10738b97c4287999`  
		Last Modified: Tue, 19 May 2026 23:43:59 GMT  
		Size: 1.2 MB (1202540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c499da7e88923de68a500a38372025709a5e929cf2d5c085e047d439a172382`  
		Last Modified: Tue, 19 May 2026 23:44:00 GMT  
		Size: 36.0 MB (35957916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bebb854df7650103650e47cb10fe57eba6c984da5edc1e288fc7bda0b6db11`  
		Last Modified: Wed, 27 May 2026 00:12:27 GMT  
		Size: 7.3 MB (7252238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:fac4d65ea67e7332de417c2d13d61e48177351efc1632557ae60880090da5b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36a664a7566bf94d44b422901d746eee3af8fd88412c9746856a5194f0b8163`

```dockerfile
```

-	Layers:
	-	`sha256:9b901c034d11e33c80379196d47bfd73dca5eb01c377b6ce77ff177067dc0e09`  
		Last Modified: Wed, 27 May 2026 00:12:27 GMT  
		Size: 2.3 MB (2298085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f9787dd257167ae8f9af48d23a1c61b99261ff6a261372f89b7e65707c6cdf`  
		Last Modified: Wed, 27 May 2026 00:12:27 GMT  
		Size: 11.5 KB (11538 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - linux; 386

```console
$ docker pull hylang@sha256:ecc39ae4f08fa6593edf06e5d3734372b227e18904bfc57e4c05dd570a98523e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73585558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d150ec4a4517fc86cccb38e34f13d17eef8e25d5eea5df5772ab2e4772303a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:34:37 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:34:37 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:34:37 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:34:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:34:37 GMT
CMD ["pypy3"]
# Wed, 27 May 2026 00:11:15 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75741b68ffe7dcd530ca760d2256e283c91857527ec2bcf75a074724c6cc2d4`  
		Last Modified: Tue, 19 May 2026 23:34:47 GMT  
		Size: 1.2 MB (1228272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dae1b058efa7fea776427e44a07cee891d3e33e2f5f20cb22283222ac29c366`  
		Last Modified: Tue, 19 May 2026 23:34:48 GMT  
		Size: 33.8 MB (33810005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5943bc35c67b54ae1a594313f331eafbbec70f18b4ebeed8d16cb14ed767409`  
		Last Modified: Wed, 27 May 2026 00:11:23 GMT  
		Size: 7.3 MB (7251946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:76a177662e907cf71d52ff985caa556e723e2d2cccb9f63019070d20311ad0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e922e2764ae761caea98da4c8501907efc571021764c4e58687c5a0f9b28e5`

```dockerfile
```

-	Layers:
	-	`sha256:b81fb8e43cd568522222485099db55b31864e3aa0254d19037e0f85a3afc67ba`  
		Last Modified: Wed, 27 May 2026 00:11:23 GMT  
		Size: 2.3 MB (2294792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7940bb20c5dfcdad26499a17b0cbaa731f2f0e2fd703015ca46d2387f7be791d`  
		Last Modified: Wed, 27 May 2026 00:11:23 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:f835cc508c923ac7f69a820dca6a84f428f5b31076d7f7b12e7b4d94ae5e2c74
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2260904533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b98302b52129b36b55c4a46dcbbd2a09877175bbf75ad6bc187b57cb60edc76`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:01 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:11 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:11 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 12 May 2026 23:50:52 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:54 GMT
CMD ["pypy"]
# Wed, 27 May 2026 00:15:04 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:15:04 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:15:57 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:15:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4498f1426c9298e6d204f6b74e5060c8b3bfb19e1328586b50b0bc0e9976829`  
		Last Modified: Tue, 12 May 2026 23:39:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88aaf7366d7bfe93d451122f3a8944fbae359f4736d40dc0fafee059a6158b43`  
		Last Modified: Tue, 12 May 2026 23:50:59 GMT  
		Size: 379.3 KB (379332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3026da7f27048853cc7e42b4ab25545ac90ec5c11d200a46b4bdc72d0b5ecf93`  
		Last Modified: Tue, 12 May 2026 23:51:04 GMT  
		Size: 15.6 MB (15559740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037c75ceed8a7791f76d2e136f20af3b0def5ba22cf6bc6559d0d6ea7835b5fe`  
		Last Modified: Tue, 12 May 2026 23:50:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cfd80338a499acab2bc1bab0a354e8d9e82c6b841f0a1548242f2adc3f4835`  
		Last Modified: Tue, 12 May 2026 23:51:03 GMT  
		Size: 30.9 MB (30932210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0ca5fe4e0cceeeb28c22eda5846c5cc99e3a968bd7dabc234bc0d05a1c444d`  
		Last Modified: Tue, 12 May 2026 23:50:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538cafec45cc5610a19568d24de1664b07401a87828d99b2a34ac2de410cb6d`  
		Last Modified: Wed, 27 May 2026 00:16:01 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41970be7d2f5bb774f1f20a5093277932b0eacf110d7f22db1d2ed3c3eb2f977`  
		Last Modified: Wed, 27 May 2026 00:16:01 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badf1ba9788e50142fc3d5f683be476a95d1921ef050f198cf987cab3c401b2b`  
		Last Modified: Wed, 27 May 2026 00:16:03 GMT  
		Size: 8.1 MB (8083509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f87bfd489017a9d7414065d25c8ed4e55a0f89a7c96771feca0c91690c698d`  
		Last Modified: Wed, 27 May 2026 00:16:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:6a2686b0dda0d8e32c01ae293ce3cdbc8ad24006d380ee4c21c2e204257e24c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177381790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1476323dd5bae7e6393f090b7925304a3f29384e480287389b73c7772b782c4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:57:01 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:57:10 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:57:10 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 12 May 2026 23:57:47 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:57:47 GMT
CMD ["pypy"]
# Wed, 27 May 2026 00:14:52 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:14:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:15:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917dd62015b1447671d0b141b1522081735e979c185e6644bec43931db85c017`  
		Last Modified: Tue, 12 May 2026 23:40:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4cff043552c33dcacac0b36ebaadff80a89cede4e38cf7eaf76bb53b102128`  
		Last Modified: Tue, 12 May 2026 23:57:54 GMT  
		Size: 485.6 KB (485554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e247f0a5b622301cd9996cbae19c8e1ac852f6224b3cb5dfa14cc80670c416b1`  
		Last Modified: Tue, 12 May 2026 23:57:55 GMT  
		Size: 15.5 MB (15527565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a0f5a85ac87f2cb41c3eb08693d43df60623a0d2222e95fa9db62166dec1b9`  
		Last Modified: Tue, 12 May 2026 23:57:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de71c613d6aa41f9b7981cb899556d4da6e2efbc880258b21126f6551ae375`  
		Last Modified: Tue, 12 May 2026 23:57:58 GMT  
		Size: 30.9 MB (30903525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cb083ae1b31bf86ac191f4ca0d052c71dda1c9810ca7c5485edcdb5aa13c6d`  
		Last Modified: Tue, 12 May 2026 23:57:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8e6be07bf3bb618dfeecc6000fa258a46f6ffbfa85a2d4a47244061927a76`  
		Last Modified: Wed, 27 May 2026 00:16:00 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871010a76d6bc092fa476b82a659e4294400a46aff139e10bf8d2d91f4bb6d75`  
		Last Modified: Wed, 27 May 2026 00:15:59 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5ba5f5177ac2c3849f2f432a85d6dc74840f1099047d8ef80ca60c2a6b6619`  
		Last Modified: Wed, 27 May 2026 00:16:01 GMT  
		Size: 8.0 MB (8036741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f0f93451339d32faa32c72e929e1d60a970b9fd4cc2580e52d879c05b6905`  
		Last Modified: Wed, 27 May 2026 00:16:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
