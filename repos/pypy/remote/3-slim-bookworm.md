## `pypy:3-slim-bookworm`

```console
$ docker pull pypy@sha256:5d7398faae93d75592e745198645b45f7b28d4904078fca2e36f96973f9614eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:e69cc76f570e5c86b2150e0d96a5559ee3b88842be22acf8b5f1ac2e2e528533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69933490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83c36acc9dac6175cee21551a769cab7b9fb95b54cd086cc3905d8d2964326`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:39:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:39:57 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:39:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:39:57 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:39:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:39:57 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a613cadd7162d1efee6ae2dd1b75c6258d7297fc77e695446cbf786646bdd1a`  
		Last Modified: Tue, 19 May 2026 23:40:09 GMT  
		Size: 3.5 MB (3511459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddd7db8cf5a9a658c95f6b8afa1dbd46e1c9d9ad0fbd46fa1f6bb027932b5eb`  
		Last Modified: Tue, 19 May 2026 23:40:10 GMT  
		Size: 38.2 MB (38188488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:8bca90f2c25d795765b53e43e99852ef1f3a63e9750aa93cff08b1f7f559a78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f4081ebe0c43cbd03f714d94f2bdbb97e006bce34a4fddc82b306434831e42`

```dockerfile
```

-	Layers:
	-	`sha256:5ba6f09dbb4aaa5a5d9adce4833afc5aa738a00fd45b131a4f3d402eb59db409`  
		Last Modified: Tue, 19 May 2026 23:40:09 GMT  
		Size: 2.7 MB (2676324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c4016cd93e99af8102f9831675f211c04edaf6b4faddc69e04c10cd99d2a235`  
		Last Modified: Tue, 19 May 2026 23:40:09 GMT  
		Size: 23.0 KB (22965 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:c3dcbce0f9b32fea58ef7818048d14a8effc2dbd5579378753fbb69ae3977a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67825865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d08e1c22c2fb0da1e84f3603a2a8db2089d7ebcd611e4db6eb15f0caaf27055`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:43:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:49 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:43:49 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:49 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:43:49 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:43:49 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395b776671cd10f7f1a8857353d3ce0354fbac555b980db222f8fec35c8975a6`  
		Last Modified: Tue, 19 May 2026 23:44:00 GMT  
		Size: 3.3 MB (3344277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a739d197e69d883112e141ae0f47158c41f80232934824844172cf826f3224`  
		Last Modified: Tue, 19 May 2026 23:44:01 GMT  
		Size: 36.4 MB (36366545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3498ff9340bf757bf5eb3f4d0c7eb42ca8e7c9c7436f89e284436cf58b02f405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa9bea9c125c5f57d04a943f05c963c5d76e2ec63f4ffac3ed2a9ce5926ad08`

```dockerfile
```

-	Layers:
	-	`sha256:3332aa8fe98fe0fb47df1a0f3ecd342ff6442a31d267e68928b4aa195119e11c`  
		Last Modified: Tue, 19 May 2026 23:44:00 GMT  
		Size: 2.7 MB (2676655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e451b888ad52dd23495665a00b47772a972ffd48778407ecd862b6a037bc4cbc`  
		Last Modified: Tue, 19 May 2026 23:44:00 GMT  
		Size: 23.1 KB (23143 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:6494a409c04c7532c8aac2a63385ce07ff1a559059a64216ed534b93c5b0548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67056962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a29f633fce506577e76d776860a1ebf3d1e44401c7334d3188a67785eb5069`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:53:58 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:53:58 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:53:58 GMT
ENV PYPY_VERSION=7.3.22
# Fri, 08 May 2026 19:53:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 08 May 2026 19:53:58 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:d90092c8edd324a692787fd4188906e71211941e12cf7df45f29d2b706aba9ab`  
		Last Modified: Fri, 08 May 2026 18:30:44 GMT  
		Size: 29.2 MB (29221767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7828cdc0dc915eea3af497ff7354178921d94652b30fd9399b6e8a7afd7c44`  
		Last Modified: Fri, 08 May 2026 19:54:09 GMT  
		Size: 3.5 MB (3514170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42c1af80231ac76ff38faf82d387a2865447309d134200f52384745d5600fd7`  
		Last Modified: Fri, 08 May 2026 19:54:10 GMT  
		Size: 34.3 MB (34321025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:5a0e1ee78acaa01d7a9211b24af56bcb94e488a7dd6082b174581006c0c62ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c81551f1e7017ad19c310718032c39c007b8cfc6eef145382cd5e10c8debc4`

```dockerfile
```

-	Layers:
	-	`sha256:710f54c9d8c7f3332de9004513226abc259a22b3744cb429ed1ca3d040e6ef2d`  
		Last Modified: Fri, 08 May 2026 19:54:09 GMT  
		Size: 2.7 MB (2673436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ac7934b184200c7f90bbc069048ffd623e8d58df1891dd0c2603e685d4c4d1`  
		Last Modified: Fri, 08 May 2026 19:54:08 GMT  
		Size: 22.9 KB (22906 bytes)  
		MIME: application/vnd.in-toto+json
