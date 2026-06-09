## `hylang:1-pypy3.11`

```console
$ docker pull hylang@sha256:204f8a65fd0f8f680d1ab57389f3fe79718fcb3768ea6a393428466fbf01df3c
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

### `hylang:1-pypy3.11` - linux; amd64

```console
$ docker pull hylang@sha256:eb225a12471e946287234e6deb5ed2af79750b883cbcac116853f6c8c2a632c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4566a7c892ff00a78d1c7ee460f7c5c2c070140154ff584dd721ac8cfa671ef3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 27 May 2026 23:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 23:37:07 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 23:37:07 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 23:37:07 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 27 May 2026 23:37:07 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 27 May 2026 23:37:07 GMT
CMD ["pypy3"]
# Mon, 08 Jun 2026 22:46:30 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:30 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fe4465a77c04781d501ea8bc062932c0af946beeb0aced76f6e2981f2e67a7`  
		Last Modified: Wed, 27 May 2026 23:37:18 GMT  
		Size: 1.2 MB (1221000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44622bc2f5f6fce499f96934420d4f6df88cfd225bab10150f01711ef8eb141`  
		Last Modified: Wed, 27 May 2026 23:37:19 GMT  
		Size: 37.8 MB (37754578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007d1b247d3ed5cf73534622ef740728dc0f2b22029961a66a07b915ce26ad03`  
		Last Modified: Mon, 08 Jun 2026 22:46:37 GMT  
		Size: 7.3 MB (7326138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:e1d5a741ef993a648473bc8bc13d8f2e7dadac76ff1258a12a84888b44411765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464de92e668b622de37826c2b415f444d625a17fd2bbeab6338e7cd28eb079a4`

```dockerfile
```

-	Layers:
	-	`sha256:f3d566ad769327b5d200c8d66c48f10c985b4be26790653a123c2bd549632e39`  
		Last Modified: Mon, 08 Jun 2026 22:46:37 GMT  
		Size: 2.3 MB (2297679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3e025b1586f11d23e57c7472932c882ee3d3bfc49475b7c44e7157df960663`  
		Last Modified: Mon, 08 Jun 2026 22:46:37 GMT  
		Size: 11.3 KB (11289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0f830e330bc62e27b3f349ce5d99625d0a71c0dd59e5d740bef19df0e192879e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74608488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef6dded405643432092f4cccffc3581af072f8406735db5d4d26f0d8b75888f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 27 May 2026 23:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 23:37:12 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 23:37:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 23:37:12 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 27 May 2026 23:37:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 27 May 2026 23:37:12 GMT
CMD ["pypy3"]
# Mon, 08 Jun 2026 22:46:50 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:50 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d98ef59115aa5e5de73aad599e72167460e924b3da19fd91c7a34eda2a1447`  
		Last Modified: Wed, 27 May 2026 23:37:23 GMT  
		Size: 1.2 MB (1202581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07ef0a74a650b39e06c32eccd8b0c4f5e436ed523882c1edbc856b4af5635e4`  
		Last Modified: Wed, 27 May 2026 23:37:24 GMT  
		Size: 35.9 MB (35937775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f926c1aab1af62e64dde7ffaa2b1727eb7ccdc228cddae7b8ed290ef00628cf`  
		Last Modified: Mon, 08 Jun 2026 22:46:57 GMT  
		Size: 7.3 MB (7326213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:d3bc3084fdba6b67c00ceeb78615559644f47e7699655e4b482d67d3218648df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaa2b17b411007bb2c4d58b32f07f2282dc85f8d6668f56c510585b9c02ea0b`

```dockerfile
```

-	Layers:
	-	`sha256:50d5aee37fb55d4f6da29a103e46ce3603cf0b3dcc83f6aa995859618fd4625d`  
		Last Modified: Mon, 08 Jun 2026 22:46:57 GMT  
		Size: 2.3 MB (2298085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246f6d8ecadfae7463756cf755851987c7a16d7849540f51660d65680340d198`  
		Last Modified: Mon, 08 Jun 2026 22:46:57 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:b7e08fbaf1ec355c8c7fa888c6ef0e056038305811a807d64cbff64223fbbb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73632202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b979f2816c6e76dbd6f9417121365920c67e7f7af33c719013281c8e3ac9de50`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Wed, 27 May 2026 23:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 23:37:18 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 23:37:18 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 23:37:18 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 27 May 2026 23:37:18 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 27 May 2026 23:37:18 GMT
CMD ["pypy3"]
# Mon, 08 Jun 2026 22:48:43 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:48:43 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:48:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:48:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57359d264662ce81bc033172474dc3050849e88ff730e746b9071f4f52848d9`  
		Last Modified: Wed, 27 May 2026 23:37:28 GMT  
		Size: 1.2 MB (1228273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf6a77b34bca8323b061d604e894a139b25065479dacd70d96eefd9d4a3aa7`  
		Last Modified: Wed, 27 May 2026 23:37:29 GMT  
		Size: 33.8 MB (33782499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5bf2d312604d080dc3e66ca90882d9ecf32cf7e557b7c4c4398b1ed7d44475`  
		Last Modified: Mon, 08 Jun 2026 22:48:51 GMT  
		Size: 7.3 MB (7326095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:b04f54d1cd6bbcb0e002c4666e1533cc25a450efbe7fd41648d52742240f88c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fde3542d706795fe8b465838653802d7d67e35cb577e71f2b785452a5a7db7`

```dockerfile
```

-	Layers:
	-	`sha256:35ae789fcda38ea36d561ac95ba3e7b2cf82530938e50b97409528f1ec84c296`  
		Last Modified: Mon, 08 Jun 2026 22:48:51 GMT  
		Size: 2.3 MB (2294792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01918977af953957216ef63e17ab1311b531d5f0066d8171678d8306bef2658f`  
		Last Modified: Mon, 08 Jun 2026 22:48:51 GMT  
		Size: 11.2 KB (11197 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:ecd1663d35f42f6fa0231261319b66d88fad2d3f92fc2a716d92753df353e2d9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261029127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20296336bcbf03ca9fa8e09bbc1e263521606953ebb8c5322e966775e51a11e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 29 May 2026 20:21:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2026 20:22:54 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 29 May 2026 20:23:31 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:23:32 GMT
ENV PYPY_VERSION=7.3.23
# Fri, 29 May 2026 20:24:25 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.23-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '948b8ea58dea5b9917210fe4afd242c788fbfaba1c3f1a25e696a404f703389a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.23-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:24:26 GMT
CMD ["pypy"]
# Mon, 08 Jun 2026 22:49:23 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:49:24 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:50:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:50:20 GMT
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
	-	`sha256:55e06cfe3090e6769e061dea81240c8e0f90ef01e4a4cbaea35363e0e0f3f1fe`  
		Last Modified: Fri, 29 May 2026 20:24:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57384028a17d77c8e25ccf0071c47db481d09c68f5e8593f1cbedd4950247f31`  
		Last Modified: Fri, 29 May 2026 20:24:32 GMT  
		Size: 408.0 KB (408042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e99a6f0964c3a9206d2ed7f18a05afa972d758418982dcdc30f9d340fcfb5e`  
		Last Modified: Fri, 29 May 2026 20:24:35 GMT  
		Size: 15.6 MB (15586360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0443f9405697d48c3057f1b0a520cb2095d01d722bc47cacbfa156e20f71a7c`  
		Last Modified: Fri, 29 May 2026 20:24:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb53bbdc77f7ce884d0663284aff705ceaf1501fbffba138fbccc4ae22b96d76`  
		Last Modified: Fri, 29 May 2026 20:24:40 GMT  
		Size: 30.9 MB (30925443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b73dc109eab7d9f35de62534949d67d5f82b99c2c8a42f55d736657345593f7`  
		Last Modified: Fri, 29 May 2026 20:24:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1312b1158b1dcb1d368929860ace0ad25e802849c23c1fb4889fd6e2d32cbeae`  
		Last Modified: Mon, 08 Jun 2026 22:50:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79cf5ce3836899e611eb3d4beb3331fe4f049823afd8bb1fe3962b992debdc2a`  
		Last Modified: Mon, 08 Jun 2026 22:50:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a816928df15a7cea9d92347e3f34ff7a970d89625afcd38d63c8a113cb0b6e8`  
		Last Modified: Mon, 08 Jun 2026 22:50:25 GMT  
		Size: 8.2 MB (8159678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2543ea25a5d7e980572dc5d94f1e2692804d88a41d57a6a98d5f243c961432f0`  
		Last Modified: Mon, 08 Jun 2026 22:50:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:f3d2b2feb4d99045b3755f0e1c37e46f83c051c05847c12a6e6f72f1746212ed
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177390325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f4171c08f7ab17a6a3babeb19f95981f5a9c7b125d15296105e5a16e442af`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 29 May 2026 20:19:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2026 20:20:44 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 29 May 2026 20:21:25 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:21:26 GMT
ENV PYPY_VERSION=7.3.23
# Fri, 29 May 2026 20:22:42 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.23-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '948b8ea58dea5b9917210fe4afd242c788fbfaba1c3f1a25e696a404f703389a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.23-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:22:44 GMT
CMD ["pypy"]
# Mon, 08 Jun 2026 22:51:50 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:51:51 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:52:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:52:50 GMT
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
	-	`sha256:8f2dd162d3f3e27f7ea1228c1d7bcca964042f02e3bcb188c8912751d041a1b8`  
		Last Modified: Fri, 29 May 2026 20:22:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f98e5a55000a966adda50bd6a691f56b0b498c14206c33d2cef26ec0a3ff1f`  
		Last Modified: Fri, 29 May 2026 20:22:49 GMT  
		Size: 510.0 KB (509983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e816cefc1a0e414cb98c1b6b66be50ca8d8f70c9b52cd65e8d18f8c7bf4513`  
		Last Modified: Fri, 29 May 2026 20:22:54 GMT  
		Size: 15.5 MB (15514989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f6384b1b5d43cb895a2823253902f38a299fa998d441930b5afc4d4d778008`  
		Last Modified: Fri, 29 May 2026 20:22:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f322e2d72b10a5b8b07ab57856f10b80787fdc0ea35db7dc60c64520b079b42f`  
		Last Modified: Fri, 29 May 2026 20:22:53 GMT  
		Size: 30.9 MB (30857888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14529cc5e2e244839a4d8d6263aa58f750074d491d3f3528c6bb48ece13086e7`  
		Last Modified: Fri, 29 May 2026 20:22:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b85ac811ee57482aafd0498781ecdaaf164f605c76c1f0c3528ce329ee7647`  
		Last Modified: Mon, 08 Jun 2026 22:52:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31f208e37873728a344a3fa21a524d3afda74fe5ed4b9583aa9f69da6911451`  
		Last Modified: Mon, 08 Jun 2026 22:52:54 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63036a890f8b9d4f7ba9be25498abbf27f14d862cb297773585e82c90c84a600`  
		Last Modified: Mon, 08 Jun 2026 22:52:55 GMT  
		Size: 8.1 MB (8079014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de656b069d79bb78ae946108b44d20f5bb79020bbcd5340fc5d041ea42efb904`  
		Last Modified: Mon, 08 Jun 2026 22:52:54 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
