## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:19bc5ed059575d861c1a3c7d5e4e60863ac72ce640a8da700bc09347eea7ccb1
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
$ docker pull pypy@sha256:ac2973e7c497a6aee64f34750edfc5d71965ab996534d7d48c55c7f95bcc2f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65871474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b156f2eb67ca810201b1e830ccbb8d318b08bc78f2ccb5293d220ed9ee4a491`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 25 Dec 2023 11:07:11 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux64.tar.bz2'; 			sha256='5938c3c6cddb2e8eb5e435cd3bf61d15134b94a9ac026e26a533bdda6c28a4a0'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-aarch64.tar.bz2'; 			sha256='98468f4cc704a2821401afdd001ebddd367e594e05a70c7767fb86f1364fb21a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux32.tar.bz2'; 			sha256='b12b4b587da55c8f212ae854e31d29258451e069c65aca596e577644e520bc8b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-s390x.tar.bz2'; 			sha256='5abc6a0f55a89c08def13b5f410b8e7bd706fe1b472f31db01ecbc4d0a49e8dc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624b94a96c3b48af9f0fef62c15f8fbd8691f7d41bc060b0f4a656fc33a363d7`  
		Last Modified: Fri, 12 Jan 2024 00:41:26 GMT  
		Size: 3.5 MB (3490953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e65a3f1d9dcf797938138aa2299a3f4a84920b8d589c3013eb8b29fd4c7ad6`  
		Last Modified: Fri, 12 Jan 2024 00:41:26 GMT  
		Size: 31.3 MB (31301932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133804d1898cb88ae00e900129af3cb7e88d01ec49aec77fdd9201a115644219`  
		Last Modified: Fri, 12 Jan 2024 00:41:25 GMT  
		Size: 2.0 MB (1952668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:7490c35071fa2e96e98074b585d5e6dd565451a54c0ce1df9f4c30604e0d3bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2060396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8349f6a7beb63800fa4a45925bc38583945e747f04c038ae6f8ff60d60500e9`

```dockerfile
```

-	Layers:
	-	`sha256:c24485fce1312e1c441439b8edc156ad093c7fa2416333a178d831e4c081966c`  
		Last Modified: Fri, 12 Jan 2024 00:41:25 GMT  
		Size: 2.0 MB (2037611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37aff3bbbea4bc9fb599f5ffb4cfba255794c1411c833a10acf429bfec493eb`  
		Last Modified: Fri, 12 Jan 2024 00:41:25 GMT  
		Size: 22.8 KB (22785 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ca4d17378b94329e0782b4ece172bcf70358e568db71b2fa19c67368bb26baca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63635985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb021b673e13ee473d027981bfe09144bd12e7b1c099aafeb44a61987d45d54`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 25 Dec 2023 11:07:11 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux64.tar.bz2'; 			sha256='5938c3c6cddb2e8eb5e435cd3bf61d15134b94a9ac026e26a533bdda6c28a4a0'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-aarch64.tar.bz2'; 			sha256='98468f4cc704a2821401afdd001ebddd367e594e05a70c7767fb86f1364fb21a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux32.tar.bz2'; 			sha256='b12b4b587da55c8f212ae854e31d29258451e069c65aca596e577644e520bc8b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-s390x.tar.bz2'; 			sha256='5abc6a0f55a89c08def13b5f410b8e7bd706fe1b472f31db01ecbc4d0a49e8dc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa08786caa4d74f3bf11ea2caa37196d90b37f529f9b8c5525bd68019cca438`  
		Last Modified: Fri, 12 Jan 2024 17:16:39 GMT  
		Size: 3.3 MB (3314054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bc7248022b30393248bc09bdc839742b0b1136a9ac5b7efcc602ea6401aab3`  
		Last Modified: Fri, 12 Jan 2024 17:25:50 GMT  
		Size: 29.2 MB (29212073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16191859300d8e0fbb4eee8bbd64f8bf28fee282a908d971350dbb541523801b`  
		Last Modified: Fri, 12 Jan 2024 17:25:48 GMT  
		Size: 2.0 MB (1952523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:ff6681b0b13eed437e497928416299eb75fa44c067abf16a52c623b0113f9daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2060573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbc151a7e3d09427a59630f8ddd19f3b4ea378b658443512afea3ed3a3dd8ac`

```dockerfile
```

-	Layers:
	-	`sha256:299c47696400c0f48147bfe399b8bec81f3df076a70f02fd380e002fbbb41d27`  
		Last Modified: Fri, 12 Jan 2024 17:25:48 GMT  
		Size: 2.0 MB (2037936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a4a0554adecb798715952c77e545c231b7a3aadc84d78bfd81c52b3f78548c`  
		Last Modified: Fri, 12 Jan 2024 17:25:48 GMT  
		Size: 22.6 KB (22637 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:9e275711986f55fe1ee14415499f1b06427dff5d433c0cbd9703de25ed798784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62334430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572fb7c47a783aa24ec3f352ea5ce94682a8f6ed6aa7c5ef9e34c7ada04a62b6`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 25 Dec 2023 11:07:11 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux64.tar.bz2'; 			sha256='5938c3c6cddb2e8eb5e435cd3bf61d15134b94a9ac026e26a533bdda6c28a4a0'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-aarch64.tar.bz2'; 			sha256='98468f4cc704a2821401afdd001ebddd367e594e05a70c7767fb86f1364fb21a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux32.tar.bz2'; 			sha256='b12b4b587da55c8f212ae854e31d29258451e069c65aca596e577644e520bc8b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-s390x.tar.bz2'; 			sha256='5abc6a0f55a89c08def13b5f410b8e7bd706fe1b472f31db01ecbc4d0a49e8dc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d26dc43c12f83c740642a6d8e07de164583691552180dbbcd6d54924b93fb`  
		Last Modified: Fri, 12 Jan 2024 00:41:25 GMT  
		Size: 3.5 MB (3496058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc4c59c06e8fa950bf4e584c2750e92bd4000bcd271a989391faa0e7136c6b9`  
		Last Modified: Fri, 12 Jan 2024 00:41:26 GMT  
		Size: 26.7 MB (26742186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418451f04ef6e11fccb65add2765cb4c8a1168ba2ba42993772037e96e0ff2e6`  
		Last Modified: Fri, 12 Jan 2024 00:41:26 GMT  
		Size: 2.0 MB (1952311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:602d273757e2bde0afa53252a40aa0d9859608d552bf45ddb93f4f6813a981e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e061076602bec49e136c217e67aeca443f259560df7de37bd81f10c10747c1`

```dockerfile
```

-	Layers:
	-	`sha256:fc159f3521cf2cf95edee15ebc37b201e0a4812b6228cfb1ca778bc98ef3c92f`  
		Last Modified: Fri, 12 Jan 2024 00:41:25 GMT  
		Size: 2.0 MB (2034839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cace620f736bdda5364fdab0484238e0627cde84193c6bea6dc3a8ede2f02a6f`  
		Last Modified: Fri, 12 Jan 2024 00:41:25 GMT  
		Size: 22.7 KB (22733 bytes)  
		MIME: application/vnd.in-toto+json
