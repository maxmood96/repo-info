## `hylang:0-pypy3.10-bullseye`

```console
$ docker pull hylang@sha256:01947295da0af980d693c8282f6ef1398d795d73fd6c6a3ec190044151d1e30f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:3bd658afcca243f84c7fdbc7fcc0b116c31c6132ab9a80e9d922baf23f3033bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72478699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad787225e3f92beb2a7ce237064cf6d2a05ba3debfc350ace964eeb56e445aec`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fa2fe7236424e81e9eb6d7f0ebc3faac63fa931fa50edccc189b2f73147307`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 863.2 KB (863163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190a3886083d340fd9dcc53e3a30570754488419876a890e3d52e0106fa5ae8`  
		Last Modified: Tue, 14 May 2024 02:58:03 GMT  
		Size: 30.5 MB (30475137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d6ec08297edc2531d4e660fe4cdcef14dfc791ea0d890ae920d833bc19138`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 3.3 MB (3300818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066e0a93a179ec365652bed1e262d7ad80ef9e1b6e5c54a87f2045a92e68be68`  
		Last Modified: Wed, 29 May 2024 22:00:35 GMT  
		Size: 6.4 MB (6405650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:66d46ae20467025dc557120541c5843ab89185caabe9afd90b1f54baee2c70c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bd08f9bf599a9339d0a39d1963e996768b1f299cdc288ff5b4b52dd0192041`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a7bdb4d7e40fe18c58f27d8779af0d739c0927c7ea25371f7a95491e30f8a`  
		Last Modified: Wed, 29 May 2024 22:00:35 GMT  
		Size: 2.7 MB (2661911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d5ed62e9d0af9798afc8dae6ea8cb7b1eb9206cf4ad47fe3baaeee5639c685`  
		Last Modified: Wed, 29 May 2024 22:00:35 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:54bcc4fda9796efad7b3b500ca66b99312c16b61d2fd9136abd510a3f69e9000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69431916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02d98bc70a5503a64d44234d5213832c10897545aec7899d61e9c17d81c9ebe`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7df0bac2bd985cd4cb39b2e9f2ddabb1dd6a3ddf35cf9b60a03597e02f19dd9`  
		Last Modified: Tue, 14 May 2024 21:39:19 GMT  
		Size: 850.5 KB (850516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03833e4eb131fd21bc43269c60a869406796a22352f4b6d37bc9c77fc7c14353`  
		Last Modified: Tue, 14 May 2024 21:39:20 GMT  
		Size: 28.8 MB (28788044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15af1c22f3e3ff43bc64682c1295d0877829ab468064cc4f2062660b8ea597b1`  
		Last Modified: Tue, 14 May 2024 21:39:19 GMT  
		Size: 3.3 MB (3300579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7674daeca331a888f9fa26b4469c3cab09944dcde6b35b44c60f9238c587f5c3`  
		Last Modified: Thu, 30 May 2024 18:41:54 GMT  
		Size: 6.4 MB (6405869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:1e07f55d01554da90b6e4fc83c9b3423970cd2837337cb6bf07f1396d0cbe6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd037cfab592a9e972fd509184356a934631c70e8ae24cca1bc5484b9bb7ba00`

```dockerfile
```

-	Layers:
	-	`sha256:957d5e3fc9a2519f693afb32f3133f663ce404d2b7453259e0226eaa018bf1a1`  
		Last Modified: Thu, 30 May 2024 18:41:54 GMT  
		Size: 2.7 MB (2662211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554d7f1643e5b032bdaa7a63286e8bbd6decb60f2a573c50b85fcca726bda04c`  
		Last Modified: Thu, 30 May 2024 18:41:53 GMT  
		Size: 9.7 KB (9718 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:e106e6c3954f524a99a8933ffb6df5a34fde09d5d52aef4450b184ec4852430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69813361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2c410399adb08ce38aabd9097ab7b5c67e70f09fe5a335cc17651ea4f973c7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4943e33d6e76cd6f17e223d464ff64415a01d77ab851208ff589e71dd2b2ad`  
		Last Modified: Tue, 14 May 2024 01:54:27 GMT  
		Size: 875.5 KB (875472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef7eec877d4784dd00414bccc1106d7583b23a7a808c76b7f14d4f2a660853c`  
		Last Modified: Tue, 14 May 2024 01:54:28 GMT  
		Size: 26.8 MB (26807182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d1638b4c8ed2e050b7c6f90bc84c4e65d7b9c3b623665f02cb1eca7797d31`  
		Last Modified: Tue, 14 May 2024 01:54:27 GMT  
		Size: 3.3 MB (3300584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70062ff2e721e84a6cd88a80e187570bc02ad414393cb1ae007072475ee343`  
		Last Modified: Wed, 29 May 2024 22:00:51 GMT  
		Size: 6.4 MB (6406080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:d005e5b8a97f4971fddbbd4464e198a6bc01f7a94bfb235e5e4d1cb638866bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cae7a5c0aedb1f9f2c6650118b473fe68d0f8b820cc572f92e9ba5f1e41c153`

```dockerfile
```

-	Layers:
	-	`sha256:85b3f225c049a89a8e4147a9bde3d17f9c238ecc76c4db3d419cc831be1d9125`  
		Last Modified: Wed, 29 May 2024 22:00:50 GMT  
		Size: 2.7 MB (2659016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fbb9ac413a7a757d76ec0659dc6c0679c22f6b258ae0863d33df5c09404083`  
		Last Modified: Wed, 29 May 2024 22:00:50 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.in-toto+json
