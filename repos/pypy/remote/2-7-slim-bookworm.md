## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:2c68d94dd481c7a90ef1636d21232cd4e95e8a1921900ad8d3f7600e1288e8c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:f881a58ee64062a21b8b7df685e3629e2ec3266881e56d3a47139bbb9228e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64824620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d27e4187ec5b1ceb653f98f523ea218367d836445043128901e7520be8d44da`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux64.tar.bz2'; 			sha256='9f3497f87b3372d17e447369e0016a4bec99a6b4d2a59aba774a25bfe4353474'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-aarch64.tar.bz2'; 			sha256='a8df5ce1650f4756933f8780870c91a0a40e7c9870d74629bf241392bcb5c2e3'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux32.tar.bz2'; 			sha256='a3aa0867cc837a34941047ece0fbb6ca190410fae6ad35fae4999d03bf178750'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b8edaa21d87a2119b5a7fefd1a7e77af19573068259c3245e7925e49b4e20`  
		Last Modified: Tue, 03 Dec 2024 02:16:07 GMT  
		Size: 3.3 MB (3306379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa4948e8572016080eb2ffdc2414d11770bb69581323004dd07c2b9c67c957`  
		Last Modified: Tue, 03 Dec 2024 02:16:08 GMT  
		Size: 31.3 MB (31333884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eec5939de3c8edf9dd937792e7c577b662a85bf77cdfd6d5202d626650b761`  
		Last Modified: Tue, 03 Dec 2024 02:16:07 GMT  
		Size: 2.0 MB (1952777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:165a7a8ff4c628dccf0ddc1ed39dec743d836402ead6e2b6a5b52422ab2fb657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85051693e4a819333447d38a4998a74973d797abc50e924a09cb93fecfe781f3`

```dockerfile
```

-	Layers:
	-	`sha256:2a7ddd9f8a2be8f9ebd05fb14b0ec0e3a3bb3577098dcdba9338175b13cc620d`  
		Last Modified: Tue, 03 Dec 2024 02:16:07 GMT  
		Size: 2.4 MB (2378848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708e9dc76ef6cee2bae4b82a45bb3998dea5f1836f813e3360e97f5ae3ae3c8c`  
		Last Modified: Tue, 03 Dec 2024 02:16:07 GMT  
		Size: 22.3 KB (22318 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:5810c17d253c7d9e683b38b6b01833f35874ee088d04c8175b12d7cf8f588b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63738612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdd27493580c7df2189494916b0836ff0966f16dd62e671ffdbd8ca38bb0917`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux64.tar.bz2'; 			sha256='9f3497f87b3372d17e447369e0016a4bec99a6b4d2a59aba774a25bfe4353474'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-aarch64.tar.bz2'; 			sha256='a8df5ce1650f4756933f8780870c91a0a40e7c9870d74629bf241392bcb5c2e3'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux32.tar.bz2'; 			sha256='a3aa0867cc837a34941047ece0fbb6ca190410fae6ad35fae4999d03bf178750'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d847e644e3906b31b79791cd7fda1c3d2196e093d2dfdc0e1f687091abfee1b3`  
		Last Modified: Tue, 12 Nov 2024 20:10:50 GMT  
		Size: 3.3 MB (3322875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafbcf5b5891841030e12954f301be51e510859836800f3466e44fc9597c34e1`  
		Last Modified: Tue, 12 Nov 2024 20:12:36 GMT  
		Size: 29.3 MB (29305696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592d0ca7ba410d37d0acf5a63cc0ada3940a0edf7f0df77cc6da0402b51ace2`  
		Last Modified: Tue, 12 Nov 2024 20:12:35 GMT  
		Size: 2.0 MB (1952685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:fbebbec12bee6967c3df6707c76da69016c449b05cb06b5bc0d5b904e6793177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77b43f5dcc66369cc297e9bf41b6d3edfd32172143f46eded9d8b1b592ba3ec`

```dockerfile
```

-	Layers:
	-	`sha256:494655d98ca46564460ac3fdd05fd31f09c4de8dc4b1515983813b8ed6911e87`  
		Last Modified: Tue, 12 Nov 2024 20:12:35 GMT  
		Size: 2.4 MB (2380400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64d4dbb3ec974110551220bbf9de47a6c95dce7779e88acd564d66efa4e086b`  
		Last Modified: Tue, 12 Nov 2024 20:12:35 GMT  
		Size: 22.5 KB (22501 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:e71dac625dd888586c47886d34735820b50e316ce9cacd3d517b18c9678d0666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61305913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e468ade2f110dbd1e86bb56d7e0a7f9c537ddb21a1bc4036ce6efed9736785`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux64.tar.bz2'; 			sha256='9f3497f87b3372d17e447369e0016a4bec99a6b4d2a59aba774a25bfe4353474'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-aarch64.tar.bz2'; 			sha256='a8df5ce1650f4756933f8780870c91a0a40e7c9870d74629bf241392bcb5c2e3'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux32.tar.bz2'; 			sha256='a3aa0867cc837a34941047ece0fbb6ca190410fae6ad35fae4999d03bf178750'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7783568cd07bf64c56e93a3ef546b73a8e2f517a1c3dddae813edad21d8cc2ee`  
		Last Modified: Tue, 03 Dec 2024 02:30:04 GMT  
		Size: 3.3 MB (3309279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c0635bfaf2778f37c16d5571e060f4552eda1d0d755c6a7bff0b1badcac018`  
		Last Modified: Tue, 03 Dec 2024 02:30:04 GMT  
		Size: 26.8 MB (26838546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df451c535043f9da43c689703e3d7f569fddf406d8c0a08281be077a8c4c613d`  
		Last Modified: Tue, 03 Dec 2024 02:30:04 GMT  
		Size: 2.0 MB (1952601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:fd6b1d1ae360c4b472e18cbc1d2015135f87bc90f3d96d6c357eb09b6cc18071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e36f58250e1c362844818187b6e41a425f77ba08d76bd068ae9f81833a8d84`

```dockerfile
```

-	Layers:
	-	`sha256:ebf461499cfa028c3d6bd68f9a79e8aea0dba2d1162c90a946a4c85018ed6701`  
		Last Modified: Tue, 03 Dec 2024 02:30:04 GMT  
		Size: 2.4 MB (2375970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3091e8224518f760b484c91fc0e2f19df4b15ad4d4805fe8e0e6ae220f76afde`  
		Last Modified: Tue, 03 Dec 2024 02:30:03 GMT  
		Size: 22.3 KB (22263 bytes)  
		MIME: application/vnd.in-toto+json
