## `hylang:pypy3.9-bookworm`

```console
$ docker pull hylang@sha256:eb894cbf87800973135dbd483d800931ccf87d5d5052d1b6eca09e557a3d6966
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
$ docker pull hylang@sha256:fb50be6af9dc42c0c05044433e34775a212ace738507b010507b7baf64385d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77788141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4ab1ac5cd9ee99eec233510ee859dacfa7dd6bf8459d24d1e42dc5898aec3c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f024c3bef872671efaa0f37104ba7501f29fb1b44f759015f32fb56540a6191`  
		Last Modified: Fri, 05 Jan 2024 18:54:36 GMT  
		Size: 3.5 MB (3490935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c3f5a11dcc88b4dca95d901891424c1818360328e5f4caaff24badf678a18`  
		Last Modified: Fri, 05 Jan 2024 18:54:37 GMT  
		Size: 37.6 MB (37556767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8238ada1064b0ecfdfdafbf4519d86a01914c720e740c1610a469004e2f278db`  
		Last Modified: Fri, 05 Jan 2024 18:54:36 GMT  
		Size: 3.3 MB (3306638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72765f594df85936849a014ab50e76aea58ecf0bab8bf6b835731d732fe99399`  
		Last Modified: Fri, 05 Jan 2024 19:48:10 GMT  
		Size: 4.3 MB (4307838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:331bfe1060161018c2e4031d43d6f97fc254e6d3d1b6f6e5367c7c2ead756567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774799babcdbf7390fb0158c1195bb43bcc709ee8e248c656e5f05d0967fb0a9`

```dockerfile
```

-	Layers:
	-	`sha256:13031867f9421a773e2f7cd9ff313e4b56e7d486eec05dcbdae6b1003e6dca54`  
		Last Modified: Fri, 05 Jan 2024 19:48:09 GMT  
		Size: 3.1 MB (3147642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4eb95ad642ccc17f0c8aa8ae838f6ac7e85cdb4113f5985a29f45b567cd085c`  
		Last Modified: Fri, 05 Jan 2024 19:48:09 GMT  
		Size: 9.8 KB (9844 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2174a425809b820a825fb56f3d1f7f0799c4db00a1dbb82895d64f2a84bc8baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74992543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fe5a61aa3fceccc73d12859189043cc090a21d10be1de6df6f70db753fccda`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb02f81cf1a233cf6e9f8f67cc4fa31d6cefb6c5f38a406131d69b8a31640fa1`  
		Last Modified: Fri, 05 Jan 2024 19:26:12 GMT  
		Size: 3.3 MB (3314096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3527c11f66ccc6572c20f1f2648fee1f22027be8f3498b9e21e25dff948d7279`  
		Last Modified: Fri, 05 Jan 2024 19:30:27 GMT  
		Size: 34.9 MB (34906388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8881d382fcc36483b90d9a400cdcfce168a268f2e71b49b6413f2ffdccb51543`  
		Last Modified: Fri, 05 Jan 2024 19:30:26 GMT  
		Size: 3.3 MB (3306796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67dd7862023065a289b27474c876cbb18d59ce716fc597785ff406f74f79bc8`  
		Last Modified: Fri, 05 Jan 2024 20:29:04 GMT  
		Size: 4.3 MB (4307994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5e88b7abaabd793dd31ce0364184a2ef7504d094ebbcc3bf559ea046eb524747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcce525828d5171aba7197a9939ab7a8013fa93d0f4b7283eedf1e27ced72181`

```dockerfile
```

-	Layers:
	-	`sha256:1500de51af2fbffe2fe6587f1700cadc9bb52a8b1b3f48a1f1ac1b38446754a5`  
		Last Modified: Fri, 05 Jan 2024 20:29:04 GMT  
		Size: 3.1 MB (3122825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff6811cfd02f906e32cfc261b3beb123b4b8cd8c2618b68e41735dd6fda6f6d`  
		Last Modified: Fri, 05 Jan 2024 20:29:03 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:e078897ff0474c7e17728451e04de8b82443bd787b66b55c838def438309014e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74670812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5679a3a648d2571f698b5e7a829dc0d523e55288b575d6d65885910315fa2b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03593a7d6250feec30aa43487ac1f00aad8cad69e84e5a4413a9f078fc1c5ae3`  
		Last Modified: Fri, 05 Jan 2024 18:54:30 GMT  
		Size: 3.5 MB (3496057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e6cdb31a5a33f3cbf42475ead2cd2db13c6b7f360fbdb0da1664a63959b34c`  
		Last Modified: Fri, 05 Jan 2024 18:54:31 GMT  
		Size: 33.4 MB (33416684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30799817807a3c0157f4866bf2199a2eec24b2c02eddf0209c8ee79f874595b`  
		Last Modified: Fri, 05 Jan 2024 18:54:30 GMT  
		Size: 3.3 MB (3306319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cb670adc098ca6f48374ed5adde719b98b96125bac5648ef433f1bf9ccda5d`  
		Last Modified: Fri, 05 Jan 2024 19:48:14 GMT  
		Size: 4.3 MB (4307889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:299a4ac2ec59cc10c2cc43ec7ce5c1db87ff2c2c7c5ad0723574413df8890347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355dc9d514ed01d77cc653921e615c6360c8afd8c6a2af4f76fba423313d80d3`

```dockerfile
```

-	Layers:
	-	`sha256:cd20205a43029a18a69355ceef56bf48ad49026490668472cfdc3abc72e0d706`  
		Last Modified: Fri, 05 Jan 2024 19:48:13 GMT  
		Size: 3.1 MB (3141963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ae3bc548051f1f48d3b862e501f355a10513d826ef38ca4986de6a72915e6b`  
		Last Modified: Fri, 05 Jan 2024 19:48:13 GMT  
		Size: 9.8 KB (9792 bytes)  
		MIME: application/vnd.in-toto+json
