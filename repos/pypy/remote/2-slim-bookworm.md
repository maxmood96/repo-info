## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:ac82171b3b6adc18ea60c6e61b629b12d17c35cb7fdb2c18a9b2007cf5b96c3d
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
$ docker pull pypy@sha256:fe4309b73d9ec3342c52e91dba820ebc1498c328f1d5096437783edab04bddf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65817774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38354bbe5e68dc69a31fa8a7b845607abb9deda39d3f973d137d5b7a0d958958`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["bash"]
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYPY_VERSION=7.3.15
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9186f7d66a062714293b112551e9cca8a48162edd97ace826e0a967d04907f1`  
		Last Modified: Tue, 13 Feb 2024 01:54:37 GMT  
		Size: 3.5 MB (3491099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a2746d9a221148879c01cdbb59f6caf5655fc7d96a8c5c5b294693507160a8`  
		Last Modified: Tue, 13 Feb 2024 01:54:37 GMT  
		Size: 31.2 MB (31249705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a5147dbf79e4f377f7b6f143d5a3836e4912028c33a494d5d79e92163224fd`  
		Last Modified: Tue, 13 Feb 2024 01:54:37 GMT  
		Size: 2.0 MB (1952879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:6444b54446d399aa269e8dc67d40221d3a8c1d5bdce9f84fc71b778d9856f03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2061388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53b4f02293d3211f9a97a5881aa4b4046b2cdd522d11528900e1c4e1057a533`

```dockerfile
```

-	Layers:
	-	`sha256:96870b8e709cc2b26f60ab55d09bd375dad0a56449050576f291539ffe438646`  
		Last Modified: Tue, 13 Feb 2024 01:54:37 GMT  
		Size: 2.0 MB (2038602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efc6bfd9a9a55c3ff360ccefcf0b1ccfcacdb52ddc3c380bad5c9c9e61bddd3e`  
		Last Modified: Tue, 13 Feb 2024 01:54:37 GMT  
		Size: 22.8 KB (22786 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:559b6652b6065dabf16ce1d597f7c2387e25fd9137b374ebcb50dc1f5646ab19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63655736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c566e217e38931b1d8a3a5f16936af48dbcea7fbde83506caf6b7cf9ee8f5256`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["bash"]
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYPY_VERSION=7.3.15
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074571ca76ee9a3c2e0926d78a1141c153886e604b5e0d672eeaae066362eac`  
		Last Modified: Wed, 14 Feb 2024 07:53:07 GMT  
		Size: 3.3 MB (3314219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e78e4f4b9a28e426644534ecfdc1551f839f4dc36596d441789d4678e5f78a`  
		Last Modified: Wed, 14 Feb 2024 08:01:17 GMT  
		Size: 29.2 MB (29232455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b497a6585bd58f926e5bfb0f12b5cee88aff0e3804098b69fe7563aaa6828af8`  
		Last Modified: Wed, 14 Feb 2024 08:01:15 GMT  
		Size: 2.0 MB (1952699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:9493a9d16d05ade7b5a452c843c1e27b88f41256b51ba09edd54b3720de55dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2061564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0edb5fca214d693cd83c3083a6fe765c1bb3263d318dcf01f5f65372bf1eb5`

```dockerfile
```

-	Layers:
	-	`sha256:37748299bd03a29ff2fa404a3fb4697c5bad4259d7da6027c5e4f4db5892b2a0`  
		Last Modified: Wed, 14 Feb 2024 08:01:15 GMT  
		Size: 2.0 MB (2038927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06772e3fee16ac965ed5ba673f1f18b090a69582515ff85025e49ce3daf9eb5a`  
		Last Modified: Wed, 14 Feb 2024 08:01:14 GMT  
		Size: 22.6 KB (22637 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:5f59c51abebff3dcd904b22c4f58aeb0595e457b79cc9c2d25620e8cf42e1bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62338641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f53b1537b6983a9218bf851bcc3bf558f4f7e1bac7077f5d7ff715e40697486`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["bash"]
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYPY_VERSION=7.3.15
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f733e4f2a2e5b1b32ad091c855095ed0a2068ebf6a587c05f32bee529a796e`  
		Last Modified: Tue, 13 Feb 2024 01:54:53 GMT  
		Size: 3.5 MB (3496213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44328877cf5f0c98c90c53c25da964648124e99b0728cfe822e72478dcbfc951`  
		Last Modified: Tue, 13 Feb 2024 01:54:54 GMT  
		Size: 26.7 MB (26748104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf2e7436da40e93b8e385dda36c177881609531c57da0f6439b1c6c6fc3f649`  
		Last Modified: Tue, 13 Feb 2024 01:54:53 GMT  
		Size: 2.0 MB (1952515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:bedde4e8b0c4ce08b1cbea2e32c4d3ee797191baed864b5c7be529d355ac6afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2058563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c466ef0e5857f4ce2e04da71bb7af4c7748574666ef1890d8f79457266378`

```dockerfile
```

-	Layers:
	-	`sha256:3f8067292e3f9c750b09b82dd57a278b918e6e00412846beeabf3885c7f235a9`  
		Last Modified: Tue, 13 Feb 2024 01:54:53 GMT  
		Size: 2.0 MB (2035830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd8c8e8c6fbc7905cddd8fd4756744ad41230ae512c0624e6df4a01734eb43a`  
		Last Modified: Tue, 13 Feb 2024 01:54:52 GMT  
		Size: 22.7 KB (22733 bytes)  
		MIME: application/vnd.in-toto+json
