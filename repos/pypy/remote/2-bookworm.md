## `pypy:2-bookworm`

```console
$ docker pull pypy@sha256:fdd6fa6d7adeafbe6e6ea43987ec8dd1b4a8845cc6f780711c31a888a4c328c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:6d595e5c2724695d67ab9563795fd9efda9037292ddd142db562b51c3c4b5fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 MB (385228896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b50682ea208f729e810125a4c4f107561fa6c55308ae9548a82467663df6a9`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 25 Dec 2023 11:07:11 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux64.tar.bz2'; 			sha256='5938c3c6cddb2e8eb5e435cd3bf61d15134b94a9ac026e26a533bdda6c28a4a0'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-aarch64.tar.bz2'; 			sha256='98468f4cc704a2821401afdd001ebddd367e594e05a70c7767fb86f1364fb21a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux32.tar.bz2'; 			sha256='b12b4b587da55c8f212ae854e31d29258451e069c65aca596e577644e520bc8b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-s390x.tar.bz2'; 			sha256='5abc6a0f55a89c08def13b5f410b8e7bd706fe1b472f31db01ecbc4d0a49e8dc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55d1cb1ffb0c7e0438b372a96cc0f23a76c21571fa3e7b7b38e3fbc66a8c3a`  
		Last Modified: Thu, 11 Jan 2024 04:44:54 GMT  
		Size: 64.1 MB (64139713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8e0026efede8b3da7364fd0ec879657b2c9be209b5cc1e2ec83bed6dfcf6a9`  
		Last Modified: Thu, 11 Jan 2024 04:45:29 GMT  
		Size: 211.1 MB (211103479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432add61fc969af941241a31f872d0af6028dd994a18ae21045601e4972cd296`  
		Last Modified: Fri, 12 Jan 2024 00:41:48 GMT  
		Size: 3.0 MB (2999192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28e890bdd457eca7b21fa63665a86dd0adbb1577e477964c0ba206ba2efc44c`  
		Last Modified: Fri, 12 Jan 2024 00:41:49 GMT  
		Size: 31.5 MB (31482502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26cc2f481a9bdf3b74dd9b7b91f0e4afdb792fa964c90afe702c1a6384a051d`  
		Last Modified: Fri, 12 Jan 2024 00:41:48 GMT  
		Size: 1.9 MB (1896026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:888f48d19d97199e7c81d0bbad86c9331b45f3cf404c3c7a639e40e9fcaf3b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13701187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58eb21d30a83c99adaef5da51c529186bf7b7c2f1ede92f1260a65fde33e6c54`

```dockerfile
```

-	Layers:
	-	`sha256:120ec938819e46d8d03e3594ab9465eae5643620d036e68d5624e89f6cba94e1`  
		Last Modified: Fri, 12 Jan 2024 00:41:49 GMT  
		Size: 13.7 MB (13676453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e52d7e4f17f09c7a7ab1d310608c109a8a154bac16e49520e56f3983b516727`  
		Last Modified: Fri, 12 Jan 2024 00:41:48 GMT  
		Size: 24.7 KB (24734 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:5d76b6bfcbb8f1a549b8df78058cdd4b813d3e5ba672edcd44a5b3b714f4eec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373948822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30f6d860d1bc04b9951fbd72dca85c7522d236235fca6253697fcd030732348`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 25 Dec 2023 11:07:11 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux64.tar.bz2'; 			sha256='5938c3c6cddb2e8eb5e435cd3bf61d15134b94a9ac026e26a533bdda6c28a4a0'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-aarch64.tar.bz2'; 			sha256='98468f4cc704a2821401afdd001ebddd367e594e05a70c7767fb86f1364fb21a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux32.tar.bz2'; 			sha256='b12b4b587da55c8f212ae854e31d29258451e069c65aca596e577644e520bc8b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-s390x.tar.bz2'; 			sha256='5abc6a0f55a89c08def13b5f410b8e7bd706fe1b472f31db01ecbc4d0a49e8dc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069a35492a4c5b1727f36b1184c413a96ce816d65578adaf3bce2023a1765c0a`  
		Last Modified: Thu, 11 Jan 2024 09:34:23 GMT  
		Size: 64.0 MB (63990799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599ff0dd2e5531872126111c843bb09b42ae90ff2d37c73e897d9e2e86c995a9`  
		Last Modified: Thu, 11 Jan 2024 09:34:53 GMT  
		Size: 202.5 MB (202501344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1fc1b8cfc32a5bb91eddb6423ba3598d04790709572847ce07857692bdf12`  
		Last Modified: Fri, 12 Jan 2024 16:53:53 GMT  
		Size: 3.0 MB (2988577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1992f79cabb0f685fb778f3f42253283189f1c9a9b60277423b872c7337c09bc`  
		Last Modified: Fri, 12 Jan 2024 17:24:15 GMT  
		Size: 29.4 MB (29397222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfca1256c16d18f651a89cd8d9333fde2203827253467c278233a2bf690cf76`  
		Last Modified: Fri, 12 Jan 2024 17:24:14 GMT  
		Size: 1.9 MB (1896041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:a0e579a995a5d02ebfda336e5042ffc59afb0f039a1aec9ad45283b493987587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13725780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930568ebb0bfdbe82bd64a7568d360a450d08478546c4c38403f8d4c2e4d7e62`

```dockerfile
```

-	Layers:
	-	`sha256:13ec065470468afdcbde409c4a7d370ddf1c8bcba9efa5e47a9f65b8b18268f1`  
		Last Modified: Fri, 12 Jan 2024 17:24:14 GMT  
		Size: 13.7 MB (13701691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939916b1827be716465eeb41d96bc8c7785965ff397c65c2612de4fdfb70281e`  
		Last Modified: Fri, 12 Jan 2024 17:24:13 GMT  
		Size: 24.1 KB (24089 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:6a721f2656a8ad9debafd564eb5f2d9bfd5cc908bd7ad46c30755be55a7f7659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383452789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b093fa35adc46cc499bf6407be29017b96ad3bca495ed6dacfb142af98b4f18b`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 25 Dec 2023 11:07:11 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux64.tar.bz2'; 			sha256='5938c3c6cddb2e8eb5e435cd3bf61d15134b94a9ac026e26a533bdda6c28a4a0'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-aarch64.tar.bz2'; 			sha256='98468f4cc704a2821401afdd001ebddd367e594e05a70c7767fb86f1364fb21a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-linux32.tar.bz2'; 			sha256='b12b4b587da55c8f212ae854e31d29258451e069c65aca596e577644e520bc8b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.14-s390x.tar.bz2'; 			sha256='5abc6a0f55a89c08def13b5f410b8e7bd706fe1b472f31db01ecbc4d0a49e8dc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:07:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:348e22f3afa19ef4ed67af4c0a3dfafe2c1311e99bde0b9039be46cafd8069f8`  
		Last Modified: Thu, 11 Jan 2024 02:42:53 GMT  
		Size: 50.6 MB (50581977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abfb5cb040b6af10cb1e9ac26bb34229604ca8c2cd52ef5bf19c4b933dd6600`  
		Last Modified: Thu, 11 Jan 2024 04:41:29 GMT  
		Size: 24.9 MB (24884306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c54028869f774208be77fae1c160385eebefa5743b2d687462a195a10b5ec1b`  
		Last Modified: Thu, 11 Jan 2024 04:41:57 GMT  
		Size: 66.0 MB (65986939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000f105af4698bd73d613c19498edc90b389261f540f976f31cc1a4f345526f`  
		Last Modified: Thu, 11 Jan 2024 04:42:52 GMT  
		Size: 210.0 MB (210036478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cdaedba4428619cee8468ba46d94c03236ee5231d91a1166c060a4d44046b`  
		Last Modified: Fri, 12 Jan 2024 00:41:36 GMT  
		Size: 3.1 MB (3142308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37cbae4215ff0cc2f9183d13ae9c55538ffbd4bbb5ef1631183c2baca34f872`  
		Last Modified: Fri, 12 Jan 2024 00:41:36 GMT  
		Size: 26.9 MB (26924734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec12db3f745e9b8d55c9fcf105e6529c5a111de77aac59a09b413e52e730d22`  
		Last Modified: Fri, 12 Jan 2024 00:41:36 GMT  
		Size: 1.9 MB (1896047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:196af7a638fbf56e64a5c588d217f38ac61e43f023354ee5f8d1f32bfb1b14d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13681533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4ab521ec96fe74e45a29ce45a992ad9eb6bafedba4eb17bf80d74a7c65941a`

```dockerfile
```

-	Layers:
	-	`sha256:d6789e5066a5baeb3dfcb425c58d41438db6914f6d0f3b791124c4e5b30a949c`  
		Last Modified: Fri, 12 Jan 2024 00:41:36 GMT  
		Size: 13.7 MB (13656853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36accde30f9259723ff5c408036288a0edd3ceb2141e6db3acc954c0de16e3e6`  
		Last Modified: Fri, 12 Jan 2024 00:41:35 GMT  
		Size: 24.7 KB (24680 bytes)  
		MIME: application/vnd.in-toto+json
