## `hylang:0-pypy3.10-bookworm`

```console
$ docker pull hylang@sha256:4eab23ee31b21c7bfab0ea70947867d3e4810926f6fa55b576dbc081c04150d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:432eacf317c44fcef3604ea0d4d7cbd0232d46240827aa62bc0aa4299d005bcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78679329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5aca15211ea17d729cf9ef7aa1fc94b53ccfea4db9c81af34e15607cea818c9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:52:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:52:57 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 02:52:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 02:52:57 GMT
ENV PYPY_VERSION=7.3.12
# Thu, 12 Oct 2023 02:53:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux64.tar.bz2'; 			sha256='6c577993160b6f5ee8cab73cd1a807affcefafe2f7441c87bd926c10505e8731'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-aarch64.tar.bz2'; 			sha256='26208b5a134d9860a08f74cce60960005758e82dc5f0e3566a48ed863a1f16a1'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux32.tar.bz2'; 			sha256='811667825ae58ada4b7c3d8bc1b5055b9f9d6a377e51aedfbe0727966603f60e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-s390x.tar.bz2'; 			sha256='043c13a585479428b463ab69575a088db74aadc16798d6e677d97f563585fee3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 12 Oct 2023 02:53:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 12 Oct 2023 02:53:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 12 Oct 2023 02:53:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 12 Oct 2023 02:53:41 GMT
CMD ["pypy3"]
# Thu, 12 Oct 2023 06:34:01 GMT
ENV HY_VERSION=0.27.0
# Thu, 12 Oct 2023 06:34:01 GMT
ENV HYRULE_VERSION=0.4.0
# Thu, 12 Oct 2023 06:34:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 12 Oct 2023 06:34:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7a35ec99b84224f62697cfb0da82b2e424c41659c7003182e565e0d22252a`  
		Last Modified: Thu, 12 Oct 2023 02:58:33 GMT  
		Size: 3.5 MB (3494482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab81c8acdec816b8125ef94d3c93b10298c5e23b35c7346b716d5663cff9a2de`  
		Last Modified: Thu, 12 Oct 2023 02:58:39 GMT  
		Size: 36.2 MB (36209154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34ddd9b67e1cfca7de88b4f3ad377a3c5ca47068bfcfc8c35df347e9d6af579`  
		Last Modified: Thu, 12 Oct 2023 02:58:33 GMT  
		Size: 3.5 MB (3513335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e61fe583383baea5fea0f202a3065ed9574de03021d93bc26632b41e3bfe99`  
		Last Modified: Thu, 12 Oct 2023 06:40:42 GMT  
		Size: 6.3 MB (6312484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:173219590ad7108cf4dce807e989a778424fd7a79174d4f79cccb4ac3781c4a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75834505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a157ca48ac5bba492d62bcf7cd47d1ee1d2ed7598e6e35d468f3e2eca1889596`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:38:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:38:34 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 03:38:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 03:38:34 GMT
ENV PYPY_VERSION=7.3.12
# Thu, 12 Oct 2023 03:40:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux64.tar.bz2'; 			sha256='6c577993160b6f5ee8cab73cd1a807affcefafe2f7441c87bd926c10505e8731'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-aarch64.tar.bz2'; 			sha256='26208b5a134d9860a08f74cce60960005758e82dc5f0e3566a48ed863a1f16a1'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux32.tar.bz2'; 			sha256='811667825ae58ada4b7c3d8bc1b5055b9f9d6a377e51aedfbe0727966603f60e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-s390x.tar.bz2'; 			sha256='043c13a585479428b463ab69575a088db74aadc16798d6e677d97f563585fee3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 12 Oct 2023 03:40:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 12 Oct 2023 03:40:15 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 12 Oct 2023 03:40:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 12 Oct 2023 03:40:28 GMT
CMD ["pypy3"]
# Thu, 12 Oct 2023 16:17:14 GMT
ENV HY_VERSION=0.27.0
# Thu, 12 Oct 2023 16:17:14 GMT
ENV HYRULE_VERSION=0.4.0
# Thu, 12 Oct 2023 16:17:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 12 Oct 2023 16:17:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f6a52ae08bd34e6b587a3267612d191904c5ca3f09aad77f727c166770e732`  
		Last Modified: Thu, 12 Oct 2023 03:52:50 GMT  
		Size: 3.3 MB (3317549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64691b5405788f729d8554b6b03b419254305d390a32660485630a8b1db8511`  
		Last Modified: Thu, 12 Oct 2023 03:52:54 GMT  
		Size: 33.5 MB (33511766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4adea4650dad01982c699dcbb7e6a851b845c4c7c0e4131ec26980df884bf5`  
		Last Modified: Thu, 12 Oct 2023 03:52:51 GMT  
		Size: 3.5 MB (3513264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975ae9de1e3ecf4449ac6e031540373df06e978f67680601e243aa6ebba647e5`  
		Last Modified: Thu, 12 Oct 2023 16:23:53 GMT  
		Size: 6.3 MB (6312642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:73005a3b122341f96c23f4dd846dbef0778339b00686a15269afae27b77a09df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78346527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8f2a1810fcec31011ee9d94379f5b3e04374b60a0b5b97d1019e134347346a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 Oct 2023 17:40:42 GMT
ADD file:31318c1b1f05d559cce42f5b12eef97d916932217e0b987fb07c0fc11bf0a14a in / 
# Wed, 11 Oct 2023 17:40:42 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 13:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 13:14:07 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 13:14:07 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 13:21:28 GMT
ENV PYPY_VERSION=7.3.13
# Thu, 26 Oct 2023 00:42:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-linux64.tar.bz2'; 			sha256='54936eeafd9350a5ea0375b036272a260871b9bca82e1b0bb3201deea9f5a442'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-aarch64.tar.bz2'; 			sha256='ac476f01c9653358404f2e4b52f62307b2f64ccdb8c96dadcbfe355824d81a63'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-linux32.tar.bz2'; 			sha256='bfba57eb1f859dd0ad0d6fe841bb12e1256f1f023c7fbca083b536cccbc1233b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-s390x.tar.bz2'; 			sha256='3c813c7efa6a026b281313b299c186c585155fc164c7538e65d41efdabff87c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Oct 2023 00:42:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 26 Oct 2023 00:42:25 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 26 Oct 2023 00:42:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Oct 2023 00:42:41 GMT
CMD ["pypy3"]
# Thu, 26 Oct 2023 01:09:13 GMT
ENV HY_VERSION=0.27.0
# Thu, 26 Oct 2023 01:09:13 GMT
ENV HYRULE_VERSION=0.4.0
# Thu, 26 Oct 2023 01:09:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 26 Oct 2023 01:09:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b27d0f1369837277a82877763487cdd2535037988fc27e16f11cf74e103ae4cd`  
		Last Modified: Wed, 11 Oct 2023 17:45:31 GMT  
		Size: 30.2 MB (30164118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210a69400fcfe838d2b3a405c5a23ac8958194459992c3cf885f15c90dc1b04`  
		Last Modified: Thu, 12 Oct 2023 13:24:51 GMT  
		Size: 3.5 MB (3499011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d762000a353cf2360d3b67e6e790ad0a19ee964f9858fbccc8f338c6eb672`  
		Last Modified: Thu, 26 Oct 2023 00:49:39 GMT  
		Size: 34.9 MB (34856352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874f46556971fe8286187e0686d7e067ca7a4c583163460b6bc3a25713740f74`  
		Last Modified: Thu, 26 Oct 2023 00:49:30 GMT  
		Size: 3.5 MB (3513310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f04adcf5ac947f384268a58c537c685621e297705642320c2c15f8acc89415`  
		Last Modified: Thu, 26 Oct 2023 01:14:42 GMT  
		Size: 6.3 MB (6313736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
