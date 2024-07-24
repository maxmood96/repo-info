## `pypy:2-7-slim`

```console
$ docker pull pypy@sha256:46fda6d8e1f46c78675e27ea5fac1025e6340695e6bc657cc61ca84de9971d70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim` - linux; amd64

```console
$ docker pull pypy@sha256:deb18cede3d9fe6a57926d93b4d6ee3106826a421b43eebe4f5044fcc4d1ed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65715923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52a75af7de22aedd507aa6950a207c2c068c0a4e57b4a0a5ba6f90f0ee477a3`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux64.tar.bz2'; 			sha256='04b2fceb712d6f811274825b8a471ee392d3d1b53afc83eb3f42439ce00d8e07'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-aarch64.tar.bz2'; 			sha256='be44e65dd8c00d2388b2580dbe2af6a5179f951a8f4979efc74360f92f3c7e96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux32.tar.bz2'; 			sha256='a19712d7a6bd4f6d113e352c5271803c583b5129b76a357d387b1fa85204f8e5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-s390x.tar.bz2'; 			sha256='09eb70b932e6aac484cf4b5f2de5845f71589f2cbb53e5ed37a497613b43cd53'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca80578ea1522cfbeadd006c4408af94cc9ea5e0b97121debb28f0535f484b3`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 1.1 MB (1066591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461f155721a0b2561246bc370673e5f9d40a2908d89fc8fe7b1c6e36744ba036`  
		Last Modified: Tue, 23 Jul 2024 07:15:53 GMT  
		Size: 31.3 MB (31265931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86549986ee0767e5a5457343b9130a60ef18191c42b0cc1eaa864d4186470fb`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 2.0 MB (1955071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:e753d275b889f9f318656d7ba41fe39708cd57b9c601bc09217c0de19e5c9707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda9ff41159cf6cfa52bae6aeb92237da29cb4e7cf452154f0cdd026dbb96d38`

```dockerfile
```

-	Layers:
	-	`sha256:642f16d9411ac364f7d351f592a4966d5c48793f326c1ebea1ab10b3e3400e89`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 2.7 MB (2664735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7c3f2d6ab7701b0f782b2c3205ca39dcbd7bb045be8e7343bf0855e80772ff`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 25.1 KB (25117 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:7ef4a0bd411ada9135998b5970771a9f045c026ff27604cd3b4044f5ed39a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62336113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263d6f4919d118a7fb59692a11fd0c085935e1b69a082f3511fd4c4056474a44`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux64.tar.bz2'; 			sha256='04b2fceb712d6f811274825b8a471ee392d3d1b53afc83eb3f42439ce00d8e07'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-aarch64.tar.bz2'; 			sha256='be44e65dd8c00d2388b2580dbe2af6a5179f951a8f4979efc74360f92f3c7e96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux32.tar.bz2'; 			sha256='a19712d7a6bd4f6d113e352c5271803c583b5129b76a357d387b1fa85204f8e5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-s390x.tar.bz2'; 			sha256='09eb70b932e6aac484cf4b5f2de5845f71589f2cbb53e5ed37a497613b43cd53'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1a87f9f75de8ddc74fffd990797d89d17b7f0d1b01c65c7e15068a4f4b21d`  
		Last Modified: Wed, 24 Jul 2024 02:05:34 GMT  
		Size: 1.1 MB (1053927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fa06d0f4b9a60d4581775612a6c307dd324ca3697e30e3416e1ab0ebf36a4f`  
		Last Modified: Wed, 24 Jul 2024 02:12:37 GMT  
		Size: 29.3 MB (29251161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416a2f488ec326ad95610865c07d51f3f1f2560f6fb54788c5b8fa1e72d23b2`  
		Last Modified: Wed, 24 Jul 2024 02:12:36 GMT  
		Size: 2.0 MB (1954942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:e3822257517cd0af4550b8b46257f2b16da8d0f4a972be274efc3a287386f327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfa8a1bd984277c576427a70f38741c951359bea0cdb1843ab6e7fa25070936`

```dockerfile
```

-	Layers:
	-	`sha256:79ea340ef24c1be4b5177bca7df3825f66d151870923930a8d7b8585c5aeee45`  
		Last Modified: Wed, 24 Jul 2024 02:12:36 GMT  
		Size: 2.7 MB (2665129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe65f18d684629e232c708a90a7da344e3f5bfe2b885922930083ae8c2af33f`  
		Last Modified: Wed, 24 Jul 2024 02:12:36 GMT  
		Size: 25.6 KB (25570 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim` - linux; 386

```console
$ docker pull pypy@sha256:0d9c2a6a7a58d5c9a7fb558d722f2a2325d3651660ec928456e14f0ebf7c31e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62212703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e066c6b2154ad83d29333957891d4d35ef3a1f5684bcdf4f04f65b11d4338826`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux64.tar.bz2'; 			sha256='04b2fceb712d6f811274825b8a471ee392d3d1b53afc83eb3f42439ce00d8e07'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-aarch64.tar.bz2'; 			sha256='be44e65dd8c00d2388b2580dbe2af6a5179f951a8f4979efc74360f92f3c7e96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux32.tar.bz2'; 			sha256='a19712d7a6bd4f6d113e352c5271803c583b5129b76a357d387b1fa85204f8e5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-s390x.tar.bz2'; 			sha256='09eb70b932e6aac484cf4b5f2de5845f71589f2cbb53e5ed37a497613b43cd53'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4912081f336596f18ecc39af8c778b1452cd28258cb4e90721f00ad2c115cb86`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 1.1 MB (1079142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ade4144e7daef2d400531c944ca3e32ce5b3002f66f44e8c4a59d15276413`  
		Last Modified: Tue, 23 Jul 2024 06:10:52 GMT  
		Size: 26.8 MB (26764819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820bff7824df185c6dd063c784966c6c3d0c80580d4d3669a4b1810b0ea13bc2`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 2.0 MB (1954934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:e680bcb46e8de258f398ff81e74393e870ca5a5294c647bc7c455d00ba884c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd32bda34b4a35a3b822955f8af239b9a05bd9e54cc9466b0e060626f72dfc`

```dockerfile
```

-	Layers:
	-	`sha256:6cdc882097d4ea176cad8a9772e5b069b923c484ef8066de034303e4a8a06474`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 2.7 MB (2661806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d07e98916b82bb28b385bbe1d787a8d5645471c41954c6b863ed89aee3fadc`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 25.0 KB (25024 bytes)  
		MIME: application/vnd.in-toto+json
