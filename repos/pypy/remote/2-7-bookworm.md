## `pypy:2-7-bookworm`

```console
$ docker pull pypy@sha256:7d81602f5358c870334a617f33b9ba1a5860dfad82a90499ec369443948a3659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:167b0b94284eb2ae6e6b323dc177f5f627b1d5a1f5bdaaac915e5b0e575e54b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381644340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070ceebbc77b6f11c38562e6cad0a1fb19c894106326749e3d51f90832dba24f`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:42 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 02:44:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:44:42 GMT
ENV PYPY_VERSION=7.3.22
# Wed, 20 May 2026 02:44:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux64.tar.bz2'; 			sha256='c47a4030542cbd34d0cb673a0de1956c94c1ebe6c6b094f2ae6a167c55375f68'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-aarch64.tar.bz2'; 			sha256='49829ef97a36d50870b0a4a7d6d67c4817d98a0bbd936e7a86ac6ef615b07205'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux32.tar.bz2'; 			sha256='3512d44a9005b52611ad2d84e63c575c8b592fb1dd1a708a00f787b46e6ee07b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 20 May 2026 02:44:42 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce041001b8968f31ff00bb8f9dbd68f72d4bdc378a1309e38eb3dfe97cc1498`  
		Last Modified: Wed, 20 May 2026 01:15:50 GMT  
		Size: 211.6 MB (211586305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cb3828f31d57993d79cd737779aaf11f0edb43038fee955b5baf46efc571b3`  
		Last Modified: Wed, 20 May 2026 02:45:01 GMT  
		Size: 33.1 MB (33114778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:37b107fa262fe1004e6a45921964c6aacf1da3ead8e3c982174450fab1d414c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15901814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9059446c02727d598c0f27cf8b0d21e40605eba1f3c0f5248eef7f6aabd6c1`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c752f990534a08786adb463c0fa079f4c678db6a05818225d9cc92adf81ed`  
		Last Modified: Wed, 20 May 2026 02:45:01 GMT  
		Size: 15.9 MB (15883279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9138483be0b08ac0bf5e4a0484f5ee57fefed7c1aad4bc8056c27969195f75e2`  
		Last Modified: Wed, 20 May 2026 02:45:00 GMT  
		Size: 18.5 KB (18535 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:cb00de7d0d170a9a6518242bdb4627d45bb33ccbdfc4787e3772bd810219250b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370572398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039e2204daa1137d0145d3887e0c03d48cca48556a811252428b5ca2b9472a57`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:45:51 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 02:45:51 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:45:51 GMT
ENV PYPY_VERSION=7.3.22
# Wed, 20 May 2026 02:45:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux64.tar.bz2'; 			sha256='c47a4030542cbd34d0cb673a0de1956c94c1ebe6c6b094f2ae6a167c55375f68'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-aarch64.tar.bz2'; 			sha256='49829ef97a36d50870b0a4a7d6d67c4817d98a0bbd936e7a86ac6ef615b07205'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux32.tar.bz2'; 			sha256='3512d44a9005b52611ad2d84e63c575c8b592fb1dd1a708a00f787b46e6ee07b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 20 May 2026 02:45:51 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03874872dc6df1c0caacf1eaa4544f492fcb08bd68a885b9b784f5e9be1d6e6`  
		Last Modified: Wed, 20 May 2026 01:15:57 GMT  
		Size: 203.1 MB (203108347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85de53242d5c42d640f1ac10c65a6bdb640e86db9c251726db75bccc90314db`  
		Last Modified: Wed, 20 May 2026 02:46:11 GMT  
		Size: 31.0 MB (30983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:213e7a2323af75444456858e6e90eb7b5885e0beae05681906b013953d3ff582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15930539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04629cd03ed85a75df433439963faf39074778965ade05a1cfef7e9d0f1d0e84`

```dockerfile
```

-	Layers:
	-	`sha256:93f54cdae152d79aec04cffb821ccbe131586b291952d4f5c93225ab5f6b6d6a`  
		Last Modified: Wed, 20 May 2026 02:46:11 GMT  
		Size: 15.9 MB (15911853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6205e67a609a9042692e831ab5e4ba47ed147443d2aefe50f088748d004f1809`  
		Last Modified: Wed, 20 May 2026 02:46:10 GMT  
		Size: 18.7 KB (18686 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:c3ff6e769e597f577a1f40ac8a95e7417e4ee596b13fbeab4e335c11c72a970e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379783036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36398356a1223dda561fc5a2a934aabcc8197b768dab7245e2eeecb5c33b19b9`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:02:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:23:31 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 06:23:31 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:23:31 GMT
ENV PYPY_VERSION=7.3.22
# Wed, 20 May 2026 06:23:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux64.tar.bz2'; 			sha256='c47a4030542cbd34d0cb673a0de1956c94c1ebe6c6b094f2ae6a167c55375f68'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-aarch64.tar.bz2'; 			sha256='49829ef97a36d50870b0a4a7d6d67c4817d98a0bbd936e7a86ac6ef615b07205'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux32.tar.bz2'; 			sha256='3512d44a9005b52611ad2d84e63c575c8b592fb1dd1a708a00f787b46e6ee07b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 20 May 2026 06:23:31 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98bd17fcd57555e95d5dbd8e55533111e892ceddbfba6eeb723b5d638807578`  
		Last Modified: Wed, 20 May 2026 06:02:48 GMT  
		Size: 210.5 MB (210513006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6e76a551dda372249f581ed92a759cfedb570c6239a3e69cf5db31b7a6e4d`  
		Last Modified: Wed, 20 May 2026 06:23:49 GMT  
		Size: 28.7 MB (28663563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:2030b246751c943a49f1c5e84ea06df273d3cf40bf0193b5784e72b57a12300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15879960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bffca039c70432a2babed9dc34da6f123b9ccaa8344b97c37da018831cf0897`

```dockerfile
```

-	Layers:
	-	`sha256:4d0916e350f483bb599c6eacf1bf88a4cb7ff72c572801ff2bceabc64a674976`  
		Last Modified: Wed, 20 May 2026 06:23:49 GMT  
		Size: 15.9 MB (15861477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe0500086a6da7520f1240f83c88cd98468c87e5169d08d174ca5f7f85f5eeb`  
		Last Modified: Wed, 20 May 2026 06:23:48 GMT  
		Size: 18.5 KB (18483 bytes)  
		MIME: application/vnd.in-toto+json
