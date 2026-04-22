## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:99d5681285f6624f81e61cce4a589e9cc6e15604aa30f66802546dfcb1cb632c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:0c2b867b6219f226842614f603ffa991de2d73ae5b04dad819305dc0e1626087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64770779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b573ac99cc39a7dd8512f70a37df3c5a1ba05921ae3619f50cd5a166d2cac`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:57:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:57:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:57:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:57:19 GMT
ENV PYPY_VERSION=7.3.21
# Wed, 22 Apr 2026 01:57:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux64.tar.bz2'; 			sha256='d560f4043180b0df5826396af17d060bd731e4fee34755167040924ece876f3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-aarch64.tar.bz2'; 			sha256='8aaed1e612e6874235ee9d5bd545a8dcc7b86c867d305351df37969390b0c47b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux32.tar.bz2'; 			sha256='14cb624e60b3012b4e5605571ab1477cea732a04e1c1385cc492d99f427a477f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 22 Apr 2026 01:57:19 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb9b6af0dc6cf4096cc8d115b9d09cada4569b88db166c28628cceaef604531`  
		Last Modified: Wed, 22 Apr 2026 01:57:29 GMT  
		Size: 3.5 MB (3510956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1249d12a2274727cf91979d20d7e55e070492733c05c501bd3965693a8b89`  
		Last Modified: Wed, 22 Apr 2026 01:57:30 GMT  
		Size: 33.0 MB (33023571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:f9a8f3e0100ef2f3a576a9aea304e28a3908894d159b246a1841e1c56b677bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fd72d3d1e0db63153a85bd185f790e0a4fd2de891d69cad221fddf51192c21`

```dockerfile
```

-	Layers:
	-	`sha256:d3d04ae4a9a0b020cff03ad62fa447e1658270237e60b06a299999f8b6e0b83e`  
		Last Modified: Wed, 22 Apr 2026 01:57:29 GMT  
		Size: 2.5 MB (2495515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dc220a78fd478158e62f4eadd89709307322a8e5339fcb1956592451560da7`  
		Last Modified: Wed, 22 Apr 2026 01:57:29 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:7b6536acd36cafd248a8122cb0a2e7c7c95ef260a76c9d949d4d465ea17f731a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62390088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4c92efbc5660635d5feee29d572c59addb360474be8829199c72ed503f46f1`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:17:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:17:28 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 02:17:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux64.tar.bz2'; 			sha256='d560f4043180b0df5826396af17d060bd731e4fee34755167040924ece876f3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-aarch64.tar.bz2'; 			sha256='8aaed1e612e6874235ee9d5bd545a8dcc7b86c867d305351df37969390b0c47b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux32.tar.bz2'; 			sha256='14cb624e60b3012b4e5605571ab1477cea732a04e1c1385cc492d99f427a477f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 02:17:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c12741a34343ddc14ea4483241583fb699d9221096614d0dcb26d7ea449c24`  
		Last Modified: Tue, 07 Apr 2026 02:17:39 GMT  
		Size: 3.3 MB (3341463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed1faf6dbadedf97beaadad451074c275a5dc58f4bf3e1d609b867138bcdb4`  
		Last Modified: Tue, 07 Apr 2026 02:17:40 GMT  
		Size: 30.9 MB (30932459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:ebd4abc95ac57a85a03f09f363daa041270f2c7060e2327ea51d859ac1e53a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2515154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f92dce2d669175a20346eb65e6914c4c1ccfefe308a5e469f657a0486039c16`

```dockerfile
```

-	Layers:
	-	`sha256:28b01336c57bf0feb0e1b5367f39645d8bdcc8f748b2869745d1618686359a88`  
		Last Modified: Tue, 07 Apr 2026 02:17:39 GMT  
		Size: 2.5 MB (2495820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a2e8bcfa2d075de4b5d08ca62f7f7dfb0009bceab95a5f7388401298d1ac70`  
		Last Modified: Tue, 07 Apr 2026 02:17:39 GMT  
		Size: 19.3 KB (19334 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:3df13bb74e1cd155554d89265b5e53a76143d66645456fa174829e146c06ca26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61317797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703eeb7711501fd61c8b49815c83b2780fd897d96bef9ef759170c9e9301ee5f`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:56:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:56:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:56:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:56:57 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 01:56:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux64.tar.bz2'; 			sha256='d560f4043180b0df5826396af17d060bd731e4fee34755167040924ece876f3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-aarch64.tar.bz2'; 			sha256='8aaed1e612e6874235ee9d5bd545a8dcc7b86c867d305351df37969390b0c47b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux32.tar.bz2'; 			sha256='14cb624e60b3012b4e5605571ab1477cea732a04e1c1385cc492d99f427a477f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 01:56:57 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd61c17d3de04748a03da44d6bd72c65aa6c599a6b7277d9c91438397bdd81`  
		Last Modified: Tue, 07 Apr 2026 01:57:06 GMT  
		Size: 3.5 MB (3512864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8bbbe3426cc6a305936ec1a9e9a7011bfc1875488f4cdeff7d93e9b143235e`  
		Last Modified: Tue, 07 Apr 2026 01:57:07 GMT  
		Size: 28.6 MB (28583165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:778ad425c482b1d11f5ff976770bd7390005a6305f2dac4c6ff5a64033c21b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9565d72a942c721a599f4a6aa6dfa93fdd45cc7ff19b1ca043a6756e59e0ea`

```dockerfile
```

-	Layers:
	-	`sha256:19199b5305f64e1a78a3e41b1bb4e94da4371765a11864f22ba1c78386b342b5`  
		Last Modified: Tue, 07 Apr 2026 01:57:06 GMT  
		Size: 2.5 MB (2492678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f8834b660d1c6b65afd80f5b2aebc4c80316bb1072bca28a271f49503e3d946`  
		Last Modified: Tue, 07 Apr 2026 01:57:06 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json
