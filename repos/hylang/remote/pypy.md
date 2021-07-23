## `hylang:pypy`

```console
$ docker pull hylang@sha256:20afca433143d7b1dd1c38f432c83b5557ee8bfa265a76a9a404295c84082155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x
	-	windows version 10.0.17763.2061; amd64

### `hylang:pypy` - linux; amd64

```console
$ docker pull hylang@sha256:f8ee2c6580423910f6c59f0c4626e1378c808707f9665b6ff61785b3637e5b00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74253095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d515c2e6ca54100cdda001a554f684d3d6c70d8452a23f9ac0c0af14908e1ac`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:43:10 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:43:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:43:11 GMT
ENV PYPY_VERSION=7.3.5
# Thu, 22 Jul 2021 14:43:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 22 Jul 2021 14:43:37 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 22 Jul 2021 14:43:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 22 Jul 2021 14:43:38 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 22 Jul 2021 14:43:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 22 Jul 2021 14:43:50 GMT
CMD ["pypy3"]
# Fri, 23 Jul 2021 10:28:42 GMT
ENV HY_VERSION=1.0a3
# Fri, 23 Jul 2021 10:28:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 23 Jul 2021 10:28:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b416d2d3e1612528c985fa1edfbee407cc2c7fb4d30f53bb6ed5ecfdd64c7a5`  
		Last Modified: Thu, 22 Jul 2021 14:46:41 GMT  
		Size: 2.8 MB (2757671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d118b8bd9ddb72dd3aa92d9cf6cf48b9663c0e4c621c9f424cd09977e5f8e5a3`  
		Last Modified: Thu, 22 Jul 2021 14:46:50 GMT  
		Size: 38.6 MB (38586599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67672d4f880c3c338d806e9ff9b3dd6ac8ea6688945b34b9e8559a9e4e4a2924`  
		Last Modified: Thu, 22 Jul 2021 14:46:41 GMT  
		Size: 2.6 MB (2598214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18089dde719af53ff508081e102b5bb75901229422060ccecdcee589f277239c`  
		Last Modified: Fri, 23 Jul 2021 10:32:19 GMT  
		Size: 3.2 MB (3164816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b0a2e837ede973d79d509b3e5e5b9a69020696249c64f16d772ae347c61d3d59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69642630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709b219af2d0a7d8cb7826d88e4b777d2ed759b08f104bb8f90878eff2167a26`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 10:20:33 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 10:20:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 10:20:33 GMT
ENV PYPY_VERSION=7.3.5
# Thu, 22 Jul 2021 10:21:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 22 Jul 2021 10:21:00 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 22 Jul 2021 10:21:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 22 Jul 2021 10:21:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 22 Jul 2021 10:21:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 22 Jul 2021 10:21:21 GMT
CMD ["pypy3"]
# Fri, 23 Jul 2021 00:15:42 GMT
ENV HY_VERSION=1.0a3
# Fri, 23 Jul 2021 00:15:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 23 Jul 2021 00:15:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d0b5d36de97ef1b3fe031873d91ef86f6bee488459e432bb22d8943b801543`  
		Last Modified: Thu, 22 Jul 2021 10:26:07 GMT  
		Size: 2.6 MB (2626319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490a19e8bbe4e083a28c764956c37e540b8f12ad1b20053624424c7e531396f4`  
		Last Modified: Thu, 22 Jul 2021 10:26:14 GMT  
		Size: 35.3 MB (35338374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3455e9b8003a51caa4862a3bf8187f6c0098adc9c529a7355ba0db203bc69a8d`  
		Last Modified: Thu, 22 Jul 2021 10:26:06 GMT  
		Size: 2.6 MB (2597921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d5b62a08fe95a11e672719a3635ad9168a1adf16a16819cd68363146cd5741`  
		Last Modified: Fri, 23 Jul 2021 00:20:45 GMT  
		Size: 3.2 MB (3165222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; 386

```console
$ docker pull hylang@sha256:405964e4082159554d7dcd2dcfc84b1722b0ea9ebf0d72600793b9e781bf3dbc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76915023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dada6df7c72e62d6336df5080d162d9791a41e2e1d79051940958ca93b642eb0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:24:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:24:37 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:24:38 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:24:38 GMT
ENV PYPY_VERSION=7.3.5
# Thu, 22 Jul 2021 15:25:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 22 Jul 2021 15:25:15 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 22 Jul 2021 15:25:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 22 Jul 2021 15:25:15 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 22 Jul 2021 15:25:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 22 Jul 2021 15:25:30 GMT
CMD ["pypy3"]
# Thu, 22 Jul 2021 23:55:14 GMT
ENV HY_VERSION=1.0a3
# Thu, 22 Jul 2021 23:55:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 22 Jul 2021 23:55:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b32ec7f2564d4cb5d38f860212b972f98c828f781a4e805ec220a1b14a0ae`  
		Last Modified: Thu, 22 Jul 2021 15:30:38 GMT  
		Size: 2.8 MB (2769392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939a00d60ec366bbd5b7f533a79aac804d3e7f1d7cbabe35cd2dae80c3e82d6`  
		Last Modified: Thu, 22 Jul 2021 15:30:48 GMT  
		Size: 40.6 MB (40585163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c4e6dee1e4deef22df36f811356aa80966a558fa9f53f558b91e5300fb04ba`  
		Last Modified: Thu, 22 Jul 2021 15:30:38 GMT  
		Size: 2.6 MB (2598046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78af76992d5276f865b0e38bc275d4cfbde940cfc61c7c01e88916d0d301aeb`  
		Last Modified: Fri, 23 Jul 2021 00:03:12 GMT  
		Size: 3.2 MB (3164963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; s390x

```console
$ docker pull hylang@sha256:68f1f5f03b6afcb6f7dba7d704dd84e8201891ed3921a831600ddd54e88adcb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69592479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e19f228791a2d3fcf841b06d51fce7f6eccdc502af8519fdd1adc040872a84`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:55:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:55:15 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:55:15 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:55:16 GMT
ENV PYPY_VERSION=7.3.5
# Thu, 22 Jul 2021 14:56:09 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 22 Jul 2021 14:56:16 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 22 Jul 2021 14:56:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 22 Jul 2021 14:56:17 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 22 Jul 2021 14:56:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 22 Jul 2021 14:56:35 GMT
CMD ["pypy3"]
# Fri, 23 Jul 2021 01:21:53 GMT
ENV HY_VERSION=1.0a3
# Fri, 23 Jul 2021 01:22:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 23 Jul 2021 01:22:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6fca19a197cb6bc4b91cc18aba2083818abd91139e8f44a16a4586fb361944`  
		Last Modified: Thu, 22 Jul 2021 14:58:38 GMT  
		Size: 2.5 MB (2452399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb3ff828255f349844582b8d04a30c215f5495ddf57c155deadf8b816a5325`  
		Last Modified: Thu, 22 Jul 2021 14:58:45 GMT  
		Size: 35.6 MB (35616132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305d8291d7a794da625ff8004d091b2b24dec421c848f50fd650bb320eadb4f3`  
		Last Modified: Thu, 22 Jul 2021 14:58:38 GMT  
		Size: 2.6 MB (2598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3457b966abc1fc372d77e8c129866b60f4004ad9257312bd7c9794c1f6731418`  
		Last Modified: Fri, 23 Jul 2021 01:24:47 GMT  
		Size: 3.2 MB (3164927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.17763.2061; amd64

```console
$ docker pull hylang@sha256:b7bd3a4f89b5bf41b8a675c247ad3dd8b69cf24644e1b98735bc010de70b5be5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2735444787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb7ba0aaf6d1cfdaf9b1c11d65867757f149cea9f1781dd0871abb5a5b0bf69`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 12:08:15 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 14 Jul 2021 12:10:43 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 Jul 2021 12:10:46 GMT
ENV PYPY_VERSION=7.3.5
# Wed, 14 Jul 2021 12:12:21 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.7-v7.3.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '072bd22427178dc4e65d961f50281bd2f56e11c4e4d9f16311c703f69f46ae24'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.7-v7.3.5-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy3 --version") ...'; 	pypy3 --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 Jul 2021 12:12:25 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 14 Jul 2021 12:12:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 14 Jul 2021 12:12:31 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 14 Jul 2021 12:14:34 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing "pip == {0}" ...' -f $env:PYTHON_PIP_VERSION); 	pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 Jul 2021 12:14:35 GMT
CMD ["pypy3"]
# Wed, 21 Jul 2021 12:01:28 GMT
ENV HY_VERSION=1.0a3
# Wed, 21 Jul 2021 12:03:10 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 21 Jul 2021 12:03:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d3a46091b43154d6b897794929e53a0f46e403377f1e821f96061cd9c2f623`  
		Last Modified: Wed, 14 Jul 2021 12:21:27 GMT  
		Size: 369.6 KB (369604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9bf609932989f7430c6ecfbaec2c55d763ef3139cad5a6ef65266664244069`  
		Last Modified: Wed, 14 Jul 2021 12:21:46 GMT  
		Size: 15.5 MB (15506661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9ecf1c520935161f5b59cf137ba65b0d7ebc50e0232f2c0f6e6b75002a79e6`  
		Last Modified: Wed, 14 Jul 2021 12:21:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f66e7f4c7774d7d6b1895c8448bd368845ca2d6e531f19d2e181a23017b15c`  
		Last Modified: Wed, 14 Jul 2021 12:21:33 GMT  
		Size: 27.0 MB (26997541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb88c235ec7d18d3dc8ef7d54c515e9430fca23a2759f14b7036f4f4eec5b2`  
		Last Modified: Wed, 14 Jul 2021 12:21:24 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bdf77c5ef17d122a55a1f3ed435649c9654f74e7b10eed007138d91fe97225`  
		Last Modified: Wed, 14 Jul 2021 12:21:24 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300875acf9d00d703ad71ab39f50c0eeff10756dcd282fa432c832903feff858`  
		Last Modified: Wed, 14 Jul 2021 12:21:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898e9c60fd7017363d46d813b2ccd43cd81243d6f37e22f4fd685bdda2cd4683`  
		Last Modified: Wed, 14 Jul 2021 12:21:25 GMT  
		Size: 3.0 MB (2950004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1733088fa35f4f7e7bdb0ca8fd69b2fca0b129597aa4100d2e14bbb751fe80c9`  
		Last Modified: Wed, 14 Jul 2021 12:21:24 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbe3c7c043c778fc3cb36628df4ec414d8f3a81fe734540e14e098bcd26453f`  
		Last Modified: Wed, 21 Jul 2021 12:03:50 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e6eadf49e9a0715fe2d2f7bde114361acec56375efc864b6ccc3773e87f25`  
		Last Modified: Wed, 21 Jul 2021 12:03:51 GMT  
		Size: 4.2 MB (4162875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cd74419baa89e4412db503319c4a993d86bfaabcf8f12a6b8925999dec5bd5`  
		Last Modified: Wed, 21 Jul 2021 12:03:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
