## `hylang:0-pypy3.10`

```console
$ docker pull hylang@sha256:38031bbe0ed3eecd2dcc40b53f36bd868b572cd3981cf25a2c5cd12d7707728d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.10` - linux; amd64

```console
$ docker pull hylang@sha256:188a72aa510dfb340f32a5e7702b9d5728d7b4013ec22586e5788bb3b93f4bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72852566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b3fb0035c72e823ca2a1b771a269f5c2de67a82c8379e0dc9a32789b20e15f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1e261ce0cd10ade4d84a8bffdfb6a25443a2929062379329f2f51ec1c44ffa`  
		Last Modified: Tue, 23 Jul 2024 07:25:20 GMT  
		Size: 3.5 MB (3495528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85382e2ae353cea7ca22fdecd394e1a87531b64c92cd4e9b62ebb50af0018fe`  
		Last Modified: Tue, 23 Jul 2024 07:25:21 GMT  
		Size: 30.5 MB (30525391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b6e93768499c551cc771bf2992c398913b0d1d58973afdd6a7c9cb4da9363`  
		Last Modified: Tue, 23 Jul 2024 07:25:20 GMT  
		Size: 3.3 MB (3299951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8b61d412f5e2a217b5454d9174671bbe3ce97998f26348f85cc1eb2a0e5480`  
		Last Modified: Tue, 23 Jul 2024 08:14:37 GMT  
		Size: 6.4 MB (6405409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:5299189e4ada3f691102af45c0c7a3efc46829ea804d32ac138d931621330fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d13adb10ecb6d1f20a3db5e39d15fb2686c000bdcd21676ae9eabc2700f7792`

```dockerfile
```

-	Layers:
	-	`sha256:5e8b97bbeefb624e067d9b28659ca38f12fc1e28f952135b0af424b3a095e6fd`  
		Last Modified: Tue, 23 Jul 2024 08:14:37 GMT  
		Size: 2.4 MB (2394814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f3dc52210aa2273125d5e4d3ec8c73f2b106ea7930efbb64c4270013273fd7`  
		Last Modified: Tue, 23 Jul 2024 08:14:37 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2fc3f7de9ad3eccf3ae1a4d23a684117db25b43bfabe0bc3ae04f0650921eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd24c256ad4ad8d17e8fad8de548059d41f86d0466837f0b3fe1df52e851945a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af27d1455dcea77106dccee118fc65f583fa379b48b33d0d5a8c3c55aa9f97f7`  
		Last Modified: Wed, 24 Jul 2024 02:03:17 GMT  
		Size: 3.3 MB (3318946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b03288750335d70660374ed8b40325a46e7eb6510ed98426aedea8fee7a29`  
		Last Modified: Wed, 24 Jul 2024 02:03:18 GMT  
		Size: 28.8 MB (28826369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61925c303d9d0798ac53021f05a40f4d56ce1f88318f6278f17f5e555f9675d7`  
		Last Modified: Wed, 24 Jul 2024 02:03:18 GMT  
		Size: 3.3 MB (3299903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af073dfab4ac608d18b437cc05e10aef460d34b32c9491dde33e23b14c99cfaf`  
		Last Modified: Wed, 24 Jul 2024 15:38:35 GMT  
		Size: 6.4 MB (6405714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:6362c94bbe537afb6cfc8520b3a88e1732b783d2434feb14c85708e3010860f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0334ff68fbdee6f0efcd5580f50b577585943776109f2d7fa37b826267115092`

```dockerfile
```

-	Layers:
	-	`sha256:883bc9adf5b6c2eeb52c14061ad906683efae955e8989d9f4bb19406f991dc7b`  
		Last Modified: Wed, 24 Jul 2024 15:38:35 GMT  
		Size: 2.4 MB (2395216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0e57d0e0a28973373c61e70c3fbe33a15782621405299ad27b7fff318a76f9`  
		Last Modified: Wed, 24 Jul 2024 15:38:34 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10` - linux; 386

```console
$ docker pull hylang@sha256:90d99669bcf1ace0461f0f02b9700ba0806583d978abdf3f41160f0d12c40d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70170909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab7a952e1502b11f7b44b9020a6a011082b9237cd8d8c6003125f47ce1283e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b074cdabb02a4f1ab960c748536d5df9705acb4c041cdb2f70ab1c409aa7db2e`  
		Last Modified: Tue, 13 Aug 2024 01:22:45 GMT  
		Size: 3.5 MB (3500279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286f00a4e1218f9f51820e88b1200e3746faf8dc38feee9c7eb45c94274bce17`  
		Last Modified: Tue, 13 Aug 2024 01:22:45 GMT  
		Size: 26.9 MB (26890553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6945b9be55b2114fc8554c775d6b4fedee0588f5cbe917c055993fc4c47ef3b`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 3.3 MB (3300602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa518307842f123166460545ac32ab14b6fecc62470a8726a11b5aac4c30eb4`  
		Last Modified: Tue, 13 Aug 2024 02:18:09 GMT  
		Size: 6.3 MB (6335194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:9b60590e98cebe7284c8635a77017b12c8e827345996c0a0c786d6ebb50a67e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9b5089f6b12fcc8d6cc1520d7ebf410567615dc48a270d9995794c4fa28025`

```dockerfile
```

-	Layers:
	-	`sha256:53a7b13bba363a8df0e8ab9d922bc42c399db87114eb7b4d9deb8c5db5595111`  
		Last Modified: Tue, 13 Aug 2024 02:18:09 GMT  
		Size: 2.4 MB (2391890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77c40ee593c21052ccf8a7af2e6e58ea7df3a296eef0b29a3a7795943f9b22`  
		Last Modified: Tue, 13 Aug 2024 02:18:09 GMT  
		Size: 11.7 KB (11670 bytes)  
		MIME: application/vnd.in-toto+json
