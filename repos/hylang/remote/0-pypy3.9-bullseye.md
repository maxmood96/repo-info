## `hylang:0-pypy3.9-bullseye`

```console
$ docker pull hylang@sha256:261aa62959c06faf4760a617433269ddcb6fd69484825365c2b8e407cd4c1831
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:2217e329c124ded35c5d54019853be12a42e134ea2dc045c227a95889b046cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69988824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e06531c0afd7fc5e4ab0dcfa3bfaa752824b97e7e2ce2d04b34e78b4e56da45`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.16
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a535fcf52cce69752fdcd53440308a29e389b2e990f78e562faa9dc18c26b0de`  
		Last Modified: Thu, 25 Apr 2024 18:53:34 GMT  
		Size: 863.2 KB (863163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c80930687f9c0f10163c4c6a2b500d19c575d3ee56d7103642a627085f489`  
		Last Modified: Thu, 25 Apr 2024 18:53:35 GMT  
		Size: 30.8 MB (30832152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a42cb356e14e7dd69b15b198bb0d1fbdcf02f93f49a6ceb3df01c6bc9f94fa9`  
		Last Modified: Thu, 25 Apr 2024 18:53:34 GMT  
		Size: 2.9 MB (2913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc201d664d27de203ffe3f09fd42eeb26061923b9791e6240450b21cca50ae`  
		Last Modified: Thu, 25 Apr 2024 19:52:43 GMT  
		Size: 3.9 MB (3945806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:97c88cd3fcfcc3f1a286197a57adea1a259d5304b7a2c576412b85aa630b13cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04da084e40700897a99eb66feb2d31bde933f1b8dcc979416a758794d56c6a`

```dockerfile
```

-	Layers:
	-	`sha256:19b9e6442787c7392186acb34a437eaf40d8d9a090c20f0ffe3dfa9a131e47b3`  
		Last Modified: Thu, 25 Apr 2024 19:52:43 GMT  
		Size: 2.7 MB (2660596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a70e44ab6c0131dbdb605313099e232566a20b434aca2e8693d3e9e882c136`  
		Last Modified: Thu, 25 Apr 2024 19:52:43 GMT  
		Size: 8.6 KB (8617 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e0996df7b90d5039fe04941faf3999835a1742cbaa4eb9c754bf2c7213c1b081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66933883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806bf32eab5c9409d048d8d4a9820782ed2d80644d479a02514b0104c00f9877`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.16
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a9efc716e9e8ba45d8e98be87ce069f03d16d552ff4ea367e5583df61358e1`  
		Last Modified: Thu, 25 Apr 2024 14:39:16 GMT  
		Size: 850.5 KB (850517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed507333861a4249502e69ede6e66f0f034938945e51649c2cee03d67218c48a`  
		Last Modified: Fri, 26 Apr 2024 08:32:07 GMT  
		Size: 29.1 MB (29136707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1422688f1bb86f99bd747b23101b320e052c42d3c475e882aff21366622de9a`  
		Last Modified: Fri, 26 Apr 2024 08:32:07 GMT  
		Size: 2.9 MB (2913348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c137f2237ab50814c66a7d1b5e6f53119cd190ca78a5cc482fd290ccf92d6c33`  
		Last Modified: Fri, 26 Apr 2024 12:41:40 GMT  
		Size: 3.9 MB (3945975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3c5684c82e68b73a4954704e9badd6c3b60d6ffa1573509b8c99079986179e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b372e6fda54addffbcbf4eb0ca86db06155595d05ade2d26027896b657c85b10`

```dockerfile
```

-	Layers:
	-	`sha256:5fbfc248ee03fd448563f90561634d687949bbaa951222046453972677120c02`  
		Last Modified: Fri, 26 Apr 2024 12:41:40 GMT  
		Size: 2.7 MB (2660803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a167eb1b7a643cefa572fe0007344c9eec9a42b70d24f8b6dd8070f03355fc64`  
		Last Modified: Fri, 26 Apr 2024 12:41:40 GMT  
		Size: 8.7 KB (8651 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:f5f4cf15a929ea14e47429acf4bd642ee3fa6e5c36ff2641cd9446da7085d980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67364717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fcf734e9844ed1eabd8b908a4b2c87d4263e23fb62cbc3ae42de1f9f71bbc9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.16
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1291a2100e9d26461578d5bc500335c7c8d3eee9f304f338fd03af9acac341f1`  
		Last Modified: Tue, 14 May 2024 01:55:19 GMT  
		Size: 875.5 KB (875452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155bed1e056750e2c46908e1ea2f7d952299d23dacf23fd9d6187ae20b68dca9`  
		Last Modified: Tue, 14 May 2024 01:55:19 GMT  
		Size: 27.2 MB (27205940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d0f12922eff3326d729a795aa520a916a8a59bced086bd950228885e91115`  
		Last Modified: Tue, 14 May 2024 01:55:18 GMT  
		Size: 2.9 MB (2913134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588625cf3dffb4fb9679f3a53ad97a8f9a71de049f09b7f25175a7ecefe153d7`  
		Last Modified: Tue, 14 May 2024 02:59:01 GMT  
		Size: 3.9 MB (3946148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e85502cf4f6df5ef47c39d0ae29256b5145d23cc0be5e22777ae2b15fd53266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9c1335c7b77373500cc47ddca2918852426112ff6dc967d7770267c87b7fd1`

```dockerfile
```

-	Layers:
	-	`sha256:0bfcea3bd1d8ea70f67f971e4ca066c25f8a2f94dd0ff80c16867d521efbd022`  
		Last Modified: Tue, 14 May 2024 02:59:01 GMT  
		Size: 2.7 MB (2657727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:287510aee7397c6bbe45248659d886776177da57a33cf05d7f523c9767bfadc4`  
		Last Modified: Tue, 14 May 2024 02:59:00 GMT  
		Size: 8.6 KB (8585 bytes)  
		MIME: application/vnd.in-toto+json
