## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:846589ed6fbcfbc62b04a119ade2980969f8fe5b97114b3b61c1afa633d23bdc
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
$ docker pull pypy@sha256:a2282c6e29242bf2528953f5f485240168b30c93e9ec545c4347394ae20e712a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65180109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9652d6696f9dfab43eb4a9631d3bc4e8571006727090eba8dbaa5389f8674346`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux64.tar.bz2'; 			sha256='1da34354e5fa59400609e94c00ba6feccf5aa575abb26fb6caf9c2ac16100ff4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-aarch64.tar.bz2'; 			sha256='d647cad5be915df65f44277fd051c8d52e708d22838b5cb21b2de033530acc80'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux32.tar.bz2'; 			sha256='54990fb1ae2266c260a7ce694b84ab91a8d0d298da440cd5695ac671dc5615e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58786be5b96b1b7d6e2607cfdaf5ba69146c0ee51ece500107deceb29c1801f2`  
		Last Modified: Fri, 07 Feb 2025 00:30:49 GMT  
		Size: 3.5 MB (3499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdfa730bdbec1c07a22003cb84faf7a3865fc3d1f5bcabf5dc359ca9fd621c8`  
		Last Modified: Fri, 07 Feb 2025 00:30:49 GMT  
		Size: 31.5 MB (31515747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57acc1c39f24fc2d01c0323d8447976f52c1b20d8dda8bf3ff26e74c020c532d`  
		Last Modified: Fri, 07 Feb 2025 00:30:49 GMT  
		Size: 2.0 MB (1952753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:e6f3828a88c0e2ad9a404b4af264dbbfae756b00a1c3b576023b2d3f788eb73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d717079424ca47a4b60f93396710ac239ed1ff5f52a8899344f02f2e1812517a`

```dockerfile
```

-	Layers:
	-	`sha256:458b723affe04d6f105dd9f04cb60e4954267aa84594f9c52a83cc1820ff9283`  
		Last Modified: Fri, 07 Feb 2025 00:30:49 GMT  
		Size: 2.4 MB (2376848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:288ad25af9e3f4f022c1a6861269a0b6a8340dbc1f94ca5c4419cdecb8529e28`  
		Last Modified: Fri, 07 Feb 2025 00:30:49 GMT  
		Size: 22.3 KB (22319 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:774e9c5c558ef6966e4fede84658ba07257e212ad8037815e9d1ef22d0d89900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62823908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20abf1447376cb35271ed62bde79a1812b73f2bf191e36563ad9404f575b7807`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux64.tar.bz2'; 			sha256='1da34354e5fa59400609e94c00ba6feccf5aa575abb26fb6caf9c2ac16100ff4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-aarch64.tar.bz2'; 			sha256='d647cad5be915df65f44277fd051c8d52e708d22838b5cb21b2de033530acc80'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux32.tar.bz2'; 			sha256='54990fb1ae2266c260a7ce694b84ab91a8d0d298da440cd5695ac671dc5615e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497bdedcf866b13dbcbbcd2f62d3716bc7a9d042292f32733123efec170975ee`  
		Last Modified: Fri, 07 Feb 2025 02:43:35 GMT  
		Size: 3.3 MB (3322844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8012eb4c1b71bf0d1c321086202d78ff828656bf730ed924c49bd96008ec5d82`  
		Last Modified: Fri, 07 Feb 2025 02:47:18 GMT  
		Size: 29.5 MB (29507484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaab6c828b25b3eec4ba75f8ef4d2ed258df3b55dd7e8af05c592d42bfc389dd`  
		Last Modified: Fri, 07 Feb 2025 02:47:18 GMT  
		Size: 2.0 MB (1952699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:ed22833a1c00895df3bd8074b7a85c2ec83c2d7af7b7e8ef7a5c9e2b85c47e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fab5f6048b0943cc14653277b9feaa8907135ae8e19bf180f1ba69f3ce9adac`

```dockerfile
```

-	Layers:
	-	`sha256:88f1f27c95c957544993b164e54a0660106de6c5d3624c03e22a472aa22bc07e`  
		Last Modified: Fri, 07 Feb 2025 02:47:18 GMT  
		Size: 2.4 MB (2377153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025a34d8e88d66e1daf3f97ba128a81eb8e29d7ea9496ed46aa25bfbbe1c8072`  
		Last Modified: Fri, 07 Feb 2025 02:47:17 GMT  
		Size: 22.5 KB (22501 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:93608aa6f977c6a11c147669e895f927d753bb66239132fed2460083b603e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61795317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad01d2494bbaa272e919215012c912800fc1c6c344d14f08d9d347494be17f63`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux64.tar.bz2'; 			sha256='1da34354e5fa59400609e94c00ba6feccf5aa575abb26fb6caf9c2ac16100ff4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-aarch64.tar.bz2'; 			sha256='d647cad5be915df65f44277fd051c8d52e708d22838b5cb21b2de033530acc80'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux32.tar.bz2'; 			sha256='54990fb1ae2266c260a7ce694b84ab91a8d0d298da440cd5695ac671dc5615e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c3e9f75652bf57c64af2371f3ad4d489d2a1169a7d99fb931a9b1928f8d16`  
		Last Modified: Fri, 07 Feb 2025 00:30:14 GMT  
		Size: 3.5 MB (3503405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25a2afb38969f18f92c45fe72841b10dee01b1127219f01a4582249bff4cbc5`  
		Last Modified: Fri, 07 Feb 2025 00:30:15 GMT  
		Size: 27.2 MB (27151941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55701cc9fe316a6fc8c1d93c0abe335dae989e70fe4a00f1428a79d71556f09e`  
		Last Modified: Fri, 07 Feb 2025 00:30:13 GMT  
		Size: 2.0 MB (1952515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:a1819386e65b7d8310540f9e0a5031dc833bd10cabdabaa12498048cffd2b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5656dce0e6eace922a8bf6dbad03e7c945d6aa811804d3a85f9220af4ad531`

```dockerfile
```

-	Layers:
	-	`sha256:9965a29282a689416e969d833174a4e12750994c5d0638d05b93b740a6b2c96d`  
		Last Modified: Fri, 07 Feb 2025 00:30:14 GMT  
		Size: 2.4 MB (2373971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa2d01f3f0164e10454b734729f4c8206c8de9719deb97c641fe4595d4e02f3`  
		Last Modified: Fri, 07 Feb 2025 00:30:13 GMT  
		Size: 22.3 KB (22263 bytes)  
		MIME: application/vnd.in-toto+json
