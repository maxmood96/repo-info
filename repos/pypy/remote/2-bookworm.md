## `pypy:2-bookworm`

```console
$ docker pull pypy@sha256:8e9d631c6e7f34b86fa26e963fd3e7b38ece05ab5cd7d88d55b598ff9b2d3620
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
$ docker pull pypy@sha256:ea7a7ba4d404c343f4a502f30fa72e4cf0ad5e8c130574e320209affccf7d0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384852702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ead4d163ac321fd9471ee27718aa0862111c2ea8eed7931fc09f79f5ba8988`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux64.tar.bz2'; 			sha256='1da34354e5fa59400609e94c00ba6feccf5aa575abb26fb6caf9c2ac16100ff4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-aarch64.tar.bz2'; 			sha256='d647cad5be915df65f44277fd051c8d52e708d22838b5cb21b2de033530acc80'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux32.tar.bz2'; 			sha256='54990fb1ae2266c260a7ce694b84ab91a8d0d298da440cd5695ac671dc5615e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f95e330ccdc77d51ce2aaa691e3c1f8bec365b16208c8b088f56fb6921773c`  
		Last Modified: Tue, 25 Feb 2025 05:12:48 GMT  
		Size: 3.0 MB (2999490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8280bb8d592891c26fa96edb075878b51dbfcc5ad74a93877f340cf57c384a6`  
		Last Modified: Tue, 25 Feb 2025 05:12:48 GMT  
		Size: 31.7 MB (31689684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6702169c8833ea27b548e04359926cbf71930697f8bfe4062aa835979a5011`  
		Last Modified: Tue, 25 Feb 2025 05:12:48 GMT  
		Size: 1.9 MB (1896039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:33f921a3768e63345e30064e707cbdc5bf2a7ccf972993354459972796e2b8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15819411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d539f077452d146693272876416f8a40bc4d3d52757075e9dac7f1893daaff5`

```dockerfile
```

-	Layers:
	-	`sha256:f9f889e536aa46395e37a8a815d2091be007cc2a07fcb1930b31153ee6f13679`  
		Last Modified: Tue, 25 Feb 2025 05:12:48 GMT  
		Size: 15.8 MB (15793381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc880ad5268bf9f899a96b5f9b5b2cddab4e6115ef945a5fcc4570e95d24471`  
		Last Modified: Tue, 25 Feb 2025 05:12:48 GMT  
		Size: 26.0 KB (26030 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ac1d0cf7e0b9f75332e8f1fbe0d217fac0c0e06b4dd4a454a7c452302fef9b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.5 MB (373544705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a9c138d58487b34ea3f60e79e941edc33b12ab49b566d65848ba9858f08eaf`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux64.tar.bz2'; 			sha256='1da34354e5fa59400609e94c00ba6feccf5aa575abb26fb6caf9c2ac16100ff4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-aarch64.tar.bz2'; 			sha256='d647cad5be915df65f44277fd051c8d52e708d22838b5cb21b2de033530acc80'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux32.tar.bz2'; 			sha256='54990fb1ae2266c260a7ce694b84ab91a8d0d298da440cd5695ac671dc5615e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c953787f592088194a8a926b92e550eed21fcb927819ef285dc8720cb5d915`  
		Last Modified: Tue, 25 Feb 2025 20:47:51 GMT  
		Size: 3.0 MB (2989456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f6ff2b268ce6e4014e7781668ff9c976892c42733307c26e017f8c6283a33e`  
		Last Modified: Tue, 25 Feb 2025 20:53:15 GMT  
		Size: 29.7 MB (29684043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce3820f98d7b1f166605cdb5f24041cc779285f99808d453535db01afed5bdf`  
		Last Modified: Tue, 25 Feb 2025 20:53:14 GMT  
		Size: 1.9 MB (1896033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:032b0e45c6dc607b5cf2bf5d0bdc13033970e0c4ab50da9f70824ea2ef6c6abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15848363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db2905cb32d2d105f8ffa029ebafa1bd33c9b53fa802c9d07c0dc5e7a39484`

```dockerfile
```

-	Layers:
	-	`sha256:233c6c2a52957cd143fa5035e9d6239a24b5233be4c9efaa01123848c9532591`  
		Last Modified: Tue, 25 Feb 2025 20:53:15 GMT  
		Size: 15.8 MB (15822055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182e07a985fafea7d5c57b76ec00d848d4e440708493318a9f25c0089a1baf8d`  
		Last Modified: Tue, 25 Feb 2025 20:53:13 GMT  
		Size: 26.3 KB (26308 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:71253d0f4c552f3897d3af6f35ee6e87bc160f68ea11d07140fed2a5f2d9c6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383221174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b186e64f4e6b00d9e634960c849811c739831acb4640599b442118e135a78025`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux64.tar.bz2'; 			sha256='1da34354e5fa59400609e94c00ba6feccf5aa575abb26fb6caf9c2ac16100ff4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-aarch64.tar.bz2'; 			sha256='d647cad5be915df65f44277fd051c8d52e708d22838b5cb21b2de033530acc80'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.18-linux32.tar.bz2'; 			sha256='54990fb1ae2266c260a7ce694b84ab91a8d0d298da440cd5695ac671dc5615e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:07:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:07:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:07:28 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3962f37c6a80e1c3d288d66e1b3bdc7ccb98aa2feac1c2978e6fcb027ed5314`  
		Last Modified: Tue, 25 Feb 2025 06:11:35 GMT  
		Size: 3.1 MB (3142658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b199eeb94e2a3f444f85f9082ccef062053a704ec0ed4a5d211d462690239`  
		Last Modified: Tue, 25 Feb 2025 06:11:35 GMT  
		Size: 27.3 MB (27331375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc09aad393ffd3f44fbf02208856d590644896cc81d1b5fe37fe6e70085ea2`  
		Last Modified: Tue, 25 Feb 2025 06:11:35 GMT  
		Size: 1.9 MB (1896040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:cfa13a2f99e88e16adc5afdc4f83787fdcf08cb19baf790f5bca291ba9a999ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15797826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020199c49bcefa99545b334f637ebed5a752da633576fd73190f7eab3ec6f3ef`

```dockerfile
```

-	Layers:
	-	`sha256:833608351a095a0552a8abc38fc7134c87cce3e4e7c2af648cd4bd6d4c48d125`  
		Last Modified: Tue, 25 Feb 2025 06:11:35 GMT  
		Size: 15.8 MB (15771892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b69e8d536e12af6c8ef1544a7974c763199baacc6b369347a25722270603bf1`  
		Last Modified: Tue, 25 Feb 2025 06:11:34 GMT  
		Size: 25.9 KB (25934 bytes)  
		MIME: application/vnd.in-toto+json
