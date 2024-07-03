## `hylang:pypy3.9-bookworm`

```console
$ docker pull hylang@sha256:fa3564f5b97860afcf22256db9b61f3b7d59cf4e33466e62cb44b0712e0187ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.9-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:1bff65f9a28bba37f59bf2f6001ffe073c772bc20f6445714ef3bc8f8d4b427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70388461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6ae6a2d757b116c00f595d5457627f4d48ef748c1b6be5f89dac4f617c78aa`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:28:19 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Wed, 24 Apr 2024 04:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
CMD ["pypy3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbf07060486135b6ef241d05633f50728fa655830c6ec2da4b560a2c32a71a5`  
		Last Modified: Tue, 02 Jul 2024 03:24:35 GMT  
		Size: 3.5 MB (3495519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527443175b6a82f09f30ece120f44e4e6873b129c97457b6b9f06c4868119d9`  
		Last Modified: Tue, 02 Jul 2024 03:24:36 GMT  
		Size: 30.9 MB (30880003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ef1d6b7460ed18772d44304308be50bacbff94f13b50850707ba33d2029e63`  
		Last Modified: Tue, 02 Jul 2024 03:24:35 GMT  
		Size: 2.9 MB (2912397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e41aa8bfd258a787d47d478a304cebe5add99c76a791a0d045b5a0e722e9ae7`  
		Last Modified: Tue, 02 Jul 2024 04:13:51 GMT  
		Size: 4.0 MB (3974264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:1076df28edb88619c3a93142d1e970bf0683cdda1559a155086b06566b9a974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1563398efe93db7c7ee2a2ca84417d6e555287a2f13fa9863a76aa5f8c1d8dff`

```dockerfile
```

-	Layers:
	-	`sha256:216f23db5b1e12a4c947aae64c2b76e2ef8b64a0a0d9f02e883183c9572bd54b`  
		Last Modified: Tue, 02 Jul 2024 04:13:51 GMT  
		Size: 2.4 MB (2370901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76236acc7f6aa3a8a23a307ccd8ee250fcc0992fcf62a1c7696b39a3e0b74a11`  
		Last Modified: Tue, 02 Jul 2024 04:13:51 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:89bdc599a52adab3b247c3738154f3433c71860b0f00789d0046281e4509b8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68538417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad1cf994bfc8e720dc358ddd68dddf975a6bcf7a3d92f611cc38ea1f26e154e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:28:19 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Wed, 24 Apr 2024 04:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
CMD ["pypy3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221aa1086ff363670f0e30eece54e6e018e35e6439b8293b66073f84dbaeb5f`  
		Last Modified: Tue, 02 Jul 2024 19:44:26 GMT  
		Size: 3.3 MB (3318953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1437192c9f83246999fa2fe393c05ee95461d53a407669926f8fbddcc7a88dc`  
		Last Modified: Tue, 02 Jul 2024 19:48:51 GMT  
		Size: 29.2 MB (29175710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228082074d58be80a26f9f4c8b32fcdc96f72c4b27ed782c4569ffd046c0e56`  
		Last Modified: Tue, 02 Jul 2024 19:48:50 GMT  
		Size: 2.9 MB (2912561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1407e08e6475b11e4576717d6ebdf7f5b9638e6b8b44368b153108c6e05ede5`  
		Last Modified: Wed, 03 Jul 2024 08:20:08 GMT  
		Size: 4.0 MB (3974630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a798b279b9135c52c9e57d59e253c25e3c3e8641489bd14100c3c6eb1c162d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9052e0eafbc25484f3d576ac33a916a9b4abec97cb047d297b6d94f1f573510`

```dockerfile
```

-	Layers:
	-	`sha256:40607c92f1457d67d0d59e418d4230676a7386b46693faea095642ace4f42744`  
		Last Modified: Wed, 03 Jul 2024 08:20:08 GMT  
		Size: 2.4 MB (2371207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a60d48cf3118612d398f1e64f6b9bbf1c43e00daa8b9059131e6d49c71b4110`  
		Last Modified: Wed, 03 Jul 2024 08:20:07 GMT  
		Size: 9.7 KB (9706 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:68518799b496d96c758c97dd26dc3e8239a1cfc2dd8c7416c8baff2de987a5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67819875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aee12011cf604ba0909c66847e44cbb564396d049bc79fb0625df4df9be3381`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:28:19 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Wed, 24 Apr 2024 04:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:28:19 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:28:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:28:19 GMT
CMD ["pypy3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9802b7ee7ae78b7d1024686bbbee25aeec1edc044812971896126cf8729d8e`  
		Last Modified: Tue, 02 Jul 2024 03:24:54 GMT  
		Size: 3.5 MB (3500294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973aa89740ce72ee81112d0f6ef0de7ed88c5fe187cc1dbd3433e65fd84bc143`  
		Last Modified: Tue, 02 Jul 2024 03:24:54 GMT  
		Size: 27.3 MB (27288879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96170cb906a44f1894035d51d219639f651b5614e2a94cc8abdd3c13a2824848`  
		Last Modified: Tue, 02 Jul 2024 03:24:53 GMT  
		Size: 2.9 MB (2912032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9a11dcc930455979c1e06742a3d72b661d6a6e0744c23203c2f3c0671d1d67`  
		Last Modified: Tue, 02 Jul 2024 04:14:19 GMT  
		Size: 4.0 MB (3974395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:9f56ff4d614cce2317d67c6d8abf5d58fe3b2d2a1315f1f40311e4935710cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d904d9197d6688386024f3031f1c105616e8942c5a40267f2e762eac5f7da5e6`

```dockerfile
```

-	Layers:
	-	`sha256:e5f23f17800ee81b17c60b5f39f3ceaba39c46955d051d9e6c564635df43c6f5`  
		Last Modified: Tue, 02 Jul 2024 04:14:18 GMT  
		Size: 2.4 MB (2368017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e468c03ffa75c230ed69348e41294a1c8459463a091933961ef33e4bd374487`  
		Last Modified: Tue, 02 Jul 2024 04:14:18 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.in-toto+json
