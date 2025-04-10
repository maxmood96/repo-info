## `pypy:3-slim`

```console
$ docker pull pypy@sha256:70f4574f3987606acc24acb9a2603801edd3d04f3e5ab9ce3c88b233c8e22fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-slim` - linux; amd64

```console
$ docker pull pypy@sha256:e6c29237c22233a494beb1e3f3e042d8cd26fe48323fb3706ce5242e62c95e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66236707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49f4416ddcbb8a98c68677a2b795451d66afbfaa26ea23c16129e061012ec3b`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f71943090982a2940a81d70af4dd1d0bf7764bdd3a97efe80acf8390fe5a30`  
		Last Modified: Wed, 09 Apr 2025 19:04:59 GMT  
		Size: 3.5 MB (3499314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d705b7ed89419c0e51a2cd2162ff8cb4e252f0053ede87b5327ac166fa78874`  
		Last Modified: Wed, 09 Apr 2025 19:05:00 GMT  
		Size: 34.5 MB (34510134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:aef7f85aa00f3d73be433766f6e585a42155d3e165d8512d38e8d8784f59216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3c8506b70d7099794552fc2bfc9d1f212f61e2ca8138483c2c728e552b2ae2`

```dockerfile
```

-	Layers:
	-	`sha256:5d7eb575e4a762f275a67ae749eff5f52b833968bcc5290668f0d235f0d9d746`  
		Last Modified: Wed, 09 Apr 2025 19:04:59 GMT  
		Size: 2.4 MB (2400169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5fbb13705bf0ec8f463b43b58970741e2da05ddd47e7669c9469c3e5e77a0e`  
		Last Modified: Wed, 09 Apr 2025 19:04:59 GMT  
		Size: 24.1 KB (24128 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:3ccbc9f1e4329b579fb337e651d378b55f5a02cc1e3f6ce971efdede1a26084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64166696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463a93db0545851528e1485ee7c5431e82bb90d62a33f50e256e04cf82a7cc3d`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d05e4cff2a664f6a67d495184f7b4a56038cfd03b22492e76175e4bba1d997`  
		Last Modified: Wed, 09 Apr 2025 21:14:57 GMT  
		Size: 3.3 MB (3322906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47240f78d63a1191ddbb464bd86a4466afa925936748e7f8b469c1b57ed53fc6`  
		Last Modified: Wed, 09 Apr 2025 21:16:51 GMT  
		Size: 32.8 MB (32777470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:b52396e5793d8357fee90433b3ce6b2db2cb37f0776d12ad5e3aa9455ba12e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca1df9e7891ca8d9f0a16d333542d0c9c462b7da29ae34835fc0dcdb9a1e089`

```dockerfile
```

-	Layers:
	-	`sha256:423c182cc8edcf1c6f692a3b36d99bea8f1f13d90b715412b6dc5120a73f8c21`  
		Last Modified: Wed, 09 Apr 2025 21:16:50 GMT  
		Size: 2.4 MB (2400596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7846bf4d53d6a92cf77e1e06a3d694dd8ab5211a89877c29f34d62f7cd0969`  
		Last Modified: Wed, 09 Apr 2025 21:16:49 GMT  
		Size: 24.4 KB (24415 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim` - linux; 386

```console
$ docker pull pypy@sha256:a5e8f3a78906fad44c1236a776c68f2e607417ec6a398d686ddb7c9a62aeaa95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63680905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3104b092667ea85909c7a7e46052270f9cd6f48f2701f3b5c45cf896146c63d1`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07cafd3a26185171039c5d13b0a11c95694ec761a8f0de8552a193d1eb6d374`  
		Last Modified: Wed, 09 Apr 2025 19:04:58 GMT  
		Size: 3.5 MB (3503459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff29eac6d6e434e953b747cd6e65f87940665d890b3c031e5cd71c17f590fc8`  
		Last Modified: Wed, 09 Apr 2025 19:04:59 GMT  
		Size: 31.0 MB (30966715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:714fad9aeddafa10a092de1728c7774843dff50daa92c4079d57adf87eb59790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2421259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab9c22bbcd7bb7281248e2f81b2aa050d1acf9411a18427554ffa43b7e1bac0`

```dockerfile
```

-	Layers:
	-	`sha256:e6a8c3311ec20079c28091096fd21be3117d3f019b1118a7a8e204ae3bc74931`  
		Last Modified: Wed, 09 Apr 2025 19:04:58 GMT  
		Size: 2.4 MB (2397236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:757c1a6a9e98c04654408499b5177acd56dfd09c1c0d990fcc9c3b8c99b0d0b9`  
		Last Modified: Wed, 09 Apr 2025 19:04:58 GMT  
		Size: 24.0 KB (24023 bytes)  
		MIME: application/vnd.in-toto+json
