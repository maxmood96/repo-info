## `pypy:2-slim-bullseye`

```console
$ docker pull pypy@sha256:1c1cffec1a5dba4ac56cd62fc7345845539802aa24703a834dac967dcb1672c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:ac98941654441618f7b3927379382e7b36910617cb0bae78495b7787f04c0d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64406045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053d333042fc73761a49c47ad57fa3c8a3440364e8acf400c4bcc59d9b5cc3d`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc20f86d30f2717b0ea14659d9c291f143c6e8e3aa202363992e79ed77f841`  
		Last Modified: Tue, 03 Dec 2024 03:20:42 GMT  
		Size: 862.5 KB (862543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b517b567ef92ce5646f0439fccee7955ef046c445de8c963c32adcf5682672`  
		Last Modified: Tue, 03 Dec 2024 03:20:42 GMT  
		Size: 31.3 MB (31335735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1f17a1c9fb59e7f5f15f29f90ee5ab6ede76a872abb909ad9f657298fc20ab`  
		Last Modified: Tue, 03 Dec 2024 03:20:42 GMT  
		Size: 2.0 MB (1955123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:7878eb864149c64c54441e6482a4e4c0f46fc2703e7577b78e8d1b7570304749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66871e63340b163b2e8d3f0a19640bbd9f57354d641c59237b48e9d4e08fde0b`

```dockerfile
```

-	Layers:
	-	`sha256:8439220c9def754cf84c56ba314ef130d698adae15e402f85904b635056cc7c2`  
		Last Modified: Tue, 03 Dec 2024 03:20:42 GMT  
		Size: 2.7 MB (2677286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ce0114ba998fa6a865721aa816b2e057fb15f7fdbe5dfd95071841eb08b221`  
		Last Modified: Tue, 03 Dec 2024 03:20:41 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:5afc3f9994814226ec4a06fd254fa602f8ad82db3cff99f7fb414253516fea27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62203714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aeb163cc27ba3b19f23bc454a5c7d7853fc9153e86a5158150e3bf60ea496b`
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930a66a25e7f585c19b8e4b37514ddbcb3bfe4b89d384937a8b80d2b8bb2e0df`  
		Last Modified: Tue, 12 Nov 2024 20:11:54 GMT  
		Size: 849.8 KB (849831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec69dc3a57128beef78c7a9ef3059e2dd8698f68d12030f4d4bdce14e303d3`  
		Last Modified: Tue, 12 Nov 2024 20:13:24 GMT  
		Size: 29.3 MB (29307288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7dad8fe5adf81a51b6c5b9eb0074c332b9c7349f7a7ccbc8aae0668ac1c9fb`  
		Last Modified: Tue, 12 Nov 2024 20:13:24 GMT  
		Size: 2.0 MB (1954995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:cac0ff9ba71715fc363cb79c272cd345ae1acba2292ecfbee3056b02e64da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eac9bebb3ade23365507b17128f55ecbd66b77fe6b28a6cc3ac9ca8fdf2d8a3`

```dockerfile
```

-	Layers:
	-	`sha256:cd3d330cec497c976ce025d1b25d6a8fa0086287ae28e9f0331c2ae605e23988`  
		Last Modified: Tue, 12 Nov 2024 20:13:23 GMT  
		Size: 2.7 MB (2679555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e1d2b7fe80e12a3eeb679ce90cd9f79848643fa669ede495ca8b733dcc436b`  
		Last Modified: Tue, 12 Nov 2024 20:13:23 GMT  
		Size: 25.0 KB (25014 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:254f98cb86854cda555fe78bd665b5593b4e4152f41449fcb6e0c611bd5473f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60850311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2eefd5d3854439e9e3450d208b9258a8966e664362e65f9ceb52138af63e548`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52270c2aba666d53bf3cd99f0f59f3d66b36ee8f09ccad91a07f97bb6e189054`  
		Last Modified: Tue, 03 Dec 2024 02:29:53 GMT  
		Size: 874.7 KB (874697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad65c14e9859d33de42cf55879e751073ab01d115a8021b5fd6b1e0116ef67`  
		Last Modified: Tue, 03 Dec 2024 02:29:54 GMT  
		Size: 26.8 MB (26841546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93448834d58896e5bbd748e72f9aed5585be8c69e76b302fe0011a06f2cef0`  
		Last Modified: Tue, 03 Dec 2024 02:29:53 GMT  
		Size: 2.0 MB (1955010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:dd4594655fca9182dde3df4d1426c2777ae8295ce6f3241cab355cbc991bde21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b95b9b3932d46d3bc0d4acde1da380176524ce8e6e7157c26ad855e517833a9`

```dockerfile
```

-	Layers:
	-	`sha256:835c6f9794725de48898caae655b7074dc1f426e70c74ebf3e8e6a0dac595582`  
		Last Modified: Tue, 03 Dec 2024 02:29:53 GMT  
		Size: 2.7 MB (2674357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f236bf4c3600d5dc554cf0c8f865f67e695d0e18bc2dfbfa9fa02244eeac34fe`  
		Last Modified: Tue, 03 Dec 2024 02:29:53 GMT  
		Size: 24.6 KB (24640 bytes)  
		MIME: application/vnd.in-toto+json
