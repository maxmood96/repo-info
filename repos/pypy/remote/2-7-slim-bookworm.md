## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:94658b9336da2208af8e07677318b82ba5862c865780acc1f5acd32cfd92c0d6
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
$ docker pull pypy@sha256:26f333b9e9ae1bd1650a01b239f4f49505b5372c4a5862cb02661f32182160db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64998388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e84c08d12e0e12c856c6db797e117e98e0dd53277dceb965fe797b59415cb0`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8eb3de64008b02a7bb3fa3ed5d3c0590a3416edb6e71af74d5d8e700146ee`  
		Last Modified: Tue, 04 Feb 2025 04:44:45 GMT  
		Size: 3.5 MB (3499322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae3371992146e2d6408cee0c7a57b9e7d3251451360d826cff86c1f31455609`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 31.3 MB (31333909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6cb2aba8da6778a0d2fd787693eacfa2176df06095d49186e163e142433d82`  
		Last Modified: Tue, 04 Feb 2025 04:44:45 GMT  
		Size: 2.0 MB (1952854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:199d9b412b8f45df42767a3711873015d271209d995b539428e99d47138668a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4025f3b8dfb32b6d1994ad324288ad5f8f1ccd9a16c4ddaac235f3d61f3944`

```dockerfile
```

-	Layers:
	-	`sha256:08873ce0b84b00de2871745f29fffd77472d96aa35d4a67107517f8c987bc8bd`  
		Last Modified: Tue, 04 Feb 2025 04:44:45 GMT  
		Size: 2.4 MB (2376838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:132025887a33f14c78cb6ded4789b442bc729c6a1d17c0e0ca9cf640b6e271a1`  
		Last Modified: Tue, 04 Feb 2025 04:44:45 GMT  
		Size: 22.3 KB (22319 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:74dfdc9c1daf386822af6cc290b84cbdfcf6f59b494f03bf703b333aac73f80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62622254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9079009b6bc6e00ede796b860beea7b3503be44cb56ab6231b4d50d84cb2e6e8`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e5450c8bac24ca222d81c4f8c837b1289ca6341bb69044c6e145b03cd881cc`  
		Last Modified: Tue, 04 Feb 2025 12:12:26 GMT  
		Size: 3.3 MB (3322847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15034e71e1cc93ec8ffc27c466c6301b7a21022a6fe3daad055663455e1fad22`  
		Last Modified: Tue, 04 Feb 2025 12:14:05 GMT  
		Size: 29.3 MB (29305688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62354eb0d709a6697a30af6cb871367a41e8ec9f579d7f0860a6926e06138961`  
		Last Modified: Tue, 04 Feb 2025 12:14:04 GMT  
		Size: 2.0 MB (1952838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:108f6805f9d4ffb9e89f3976d669a769019f2e03235941cbcee5cb22a815fe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91962d7458af58ba4d2666dd910b5cc3c640e8ae9b679bcd76f12b4a64beee3a`

```dockerfile
```

-	Layers:
	-	`sha256:b1cb55d5e73c0b537398223ac60c2c87e23bf2774a636852e575d0e4e6e7b23c`  
		Last Modified: Tue, 04 Feb 2025 12:14:04 GMT  
		Size: 2.4 MB (2377143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ebd1001f4d4e7d8b59d404084896ccaf92a1b0d1608c4eb0c278fd6ab7d524`  
		Last Modified: Tue, 04 Feb 2025 12:14:03 GMT  
		Size: 22.5 KB (22500 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:518395f86b16d3ff6b3203b883a9ab1bfa6a5d054b9696f0595b15fab938b80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e674ed3d0e819325e59bd625d1b2c72f6a9ca4e463f6f54f43b97ed50ab8640b`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 28 Aug 2024 10:07:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb2fb331b96e13bca8f24848fdb30aa0fb7f6269624d3f3ecee874542029312`  
		Last Modified: Tue, 04 Feb 2025 04:39:08 GMT  
		Size: 3.5 MB (3503412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75461dcc168fe5f8e1a03a36a18a0cbc52cd3ed15b2d829b63f0b96e991f166`  
		Last Modified: Tue, 04 Feb 2025 04:39:09 GMT  
		Size: 26.8 MB (26838530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeff635b436fa79a9a446798180147d274bcc33e5764f2ba5ba6f18015b1fa0`  
		Last Modified: Tue, 04 Feb 2025 04:39:08 GMT  
		Size: 2.0 MB (1952581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:d40b6fec2574a270df2de39054e27890654058ab375f5ca00aed5629b55959c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f50b9ab98c4c04fdda37c2a97a34380f7e3bd69ad4f637e7d2e7decaca8ae1`

```dockerfile
```

-	Layers:
	-	`sha256:bd7f3073ade2bf8ecc6b0b41f1d3e7c83234a287d96b5e95b59fc5af629d971c`  
		Last Modified: Tue, 04 Feb 2025 04:39:08 GMT  
		Size: 2.4 MB (2373961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0935ad7b969823640f90d76b30e35ae189a56769d6e0ee5aff2f650f4e7f568`  
		Last Modified: Tue, 04 Feb 2025 04:39:08 GMT  
		Size: 22.3 KB (22263 bytes)  
		MIME: application/vnd.in-toto+json
