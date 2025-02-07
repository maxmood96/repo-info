## `pypy:2-slim-bullseye`

```console
$ docker pull pypy@sha256:3b1b9dcaf32a6635eff0d8c7ac04ca8b988b8b82396dde794d9722d49bccea92
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
$ docker pull pypy@sha256:5c903d7accf9bd56f8fb6d6f657b81fdbeee3a10380cfeca05ab95da31752935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64588161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f27e50265d5b559990707239309683885882e71c0c12ab1e8548f94272bda0`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097f5ad145d2afd6f45519827a162ee1ed77f31dcba1fe2983be044e11115e`  
		Last Modified: Fri, 07 Feb 2025 00:31:07 GMT  
		Size: 862.6 KB (862575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae0a321836e009785094c90e7f2b335329999a1622ca9e526a23143efe44a9f`  
		Last Modified: Fri, 07 Feb 2025 00:31:09 GMT  
		Size: 31.5 MB (31517856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e661df70c1bde00dfc7afe306857e285fe8f30a7d6b383a38723d1be80b0aa`  
		Last Modified: Fri, 07 Feb 2025 00:31:08 GMT  
		Size: 2.0 MB (1955142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:9e7338933b904ff2ee3ce9b9d454519db8ac6177f9d92bf495b1b043bfc7ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef6daae850768f3dab0d57d668c2d6d855d20097ef255461f78d816908226c0`

```dockerfile
```

-	Layers:
	-	`sha256:d736b36715ca82296e968c882093dc4cfb6922ae659c9e2a2bc41699f58e008a`  
		Last Modified: Fri, 07 Feb 2025 00:31:08 GMT  
		Size: 2.7 MB (2674593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16f641c7aa3501bb09a4f7ee1cd65058d9b5b76485bb826f2ca60c43be24718`  
		Last Modified: Fri, 07 Feb 2025 00:31:07 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ce07550c9075d0961b9d9bbeff2d4d8c81c4b6a2fa69819f4f41e2136ced054b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61058953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d10f3664bd3cf2d6e508d4e55130b2e30e05d82b9ebcf04b2b7d2f6d286f6af`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4969a1bce34493ffc6bc24d7940543e7241420f3d3f8f43badd0c29ec743847`  
		Last Modified: Fri, 07 Feb 2025 02:45:45 GMT  
		Size: 849.8 KB (849789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722c32869aab74ebc406e194e4f552f0c4d56d8566bfcc9ef3eedb9a7d64bdd`  
		Last Modified: Fri, 07 Feb 2025 02:48:46 GMT  
		Size: 29.5 MB (29509230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163742c111b13626f4f03da1b23addf31f257a0a4a8c17da1ee484a00a342f0`  
		Last Modified: Fri, 07 Feb 2025 02:48:45 GMT  
		Size: 2.0 MB (1955124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:7e1381b43dd51c751ca840e387e7eaf8b129234370e7d79dfaed2a6de2773b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd4b24c2cfe13a0928c5e282ba2dbb07d0371ef88b4622a3356e69cb013c9c6`

```dockerfile
```

-	Layers:
	-	`sha256:099648ed125b053f656ffb32df1efc0a671ef856393008ce09fd68e1c8a172bb`  
		Last Modified: Fri, 07 Feb 2025 02:48:45 GMT  
		Size: 2.7 MB (2674988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a28547af17d61eae68f071a7e752fb7d4f5538e6565cb235469e8092640dbf`  
		Last Modified: Fri, 07 Feb 2025 02:48:44 GMT  
		Size: 25.0 KB (25014 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:3d3f5b344243d2dd89229ea552daf67d3b6f985759cee8d8ac4cef5f8aa92590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61163074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925cefcf27d905eb8f59ac301b15fca5cd9435aa050adf76cdce5001dff0e655`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
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
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884617f6d9ccc2e623f2ecfd14e38fb73fb5f7fe9737509310fd63cf4df4b46`  
		Last Modified: Fri, 07 Feb 2025 00:30:20 GMT  
		Size: 874.7 KB (874683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6e3a30f3fdc31f4c60e1373b264d4d3f7ecd3aff6087194c91ce0f639eeb8`  
		Last Modified: Fri, 07 Feb 2025 00:30:21 GMT  
		Size: 27.2 MB (27154638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0c5ffedbba1218e6b7921d547f1a69a8d11fc35c0d3fc64d26e810c799eb7d`  
		Last Modified: Fri, 07 Feb 2025 00:30:20 GMT  
		Size: 2.0 MB (1954878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:10976feaadd38b613f547d39d98db0991fed6d5e85b4aa517a2bad32d97b382b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439ed97cf0e6c791b39ea0ea5f2a4202846239f06b21c8383b078863e15a321e`

```dockerfile
```

-	Layers:
	-	`sha256:f34800ea8949f87f9c1cabd5ef324913e1f556fc9af978c5d8e7b56aca0ab6a0`  
		Last Modified: Fri, 07 Feb 2025 00:30:20 GMT  
		Size: 2.7 MB (2671665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f46aca429c3c5a12093cad42a7f13e26c44191f6783c7a09e4cdb7fa7f6ec2c`  
		Last Modified: Fri, 07 Feb 2025 00:30:20 GMT  
		Size: 24.6 KB (24640 bytes)  
		MIME: application/vnd.in-toto+json
