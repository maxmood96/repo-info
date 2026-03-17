## `pypy:2-bookworm`

```console
$ docker pull pypy@sha256:77a8a6e0174ecd0ee559a977901e297436ff35f098997793b6d8f3176e73cbd6
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
$ docker pull pypy@sha256:276ca2c3c5aa09662f7103dbd644c481370540e27dd547865da93ecd89df1c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381422923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e8fbb10931ed0ac2b2f55b7a24b1118a6671a9d49348192629c9f3ffe70761`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:06:40 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:06:40 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:06:40 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 17 Mar 2026 02:06:40 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux64.tar.bz2'; 			sha256='d560f4043180b0df5826396af17d060bd731e4fee34755167040924ece876f3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-aarch64.tar.bz2'; 			sha256='8aaed1e612e6874235ee9d5bd545a8dcc7b86c867d305351df37969390b0c47b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux32.tar.bz2'; 			sha256='14cb624e60b3012b4e5605571ab1477cea732a04e1c1385cc492d99f427a477f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 17 Mar 2026 02:06:40 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505954b662451663b30768d461d6881e47bb272f6bc64e4d297f5cf79b9000cb`  
		Last Modified: Tue, 17 Mar 2026 00:20:24 GMT  
		Size: 211.5 MB (211529392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65f3a9c8c273d5a953df3cf69b05de45a5ec1823a82c3a344ae68c39916a50`  
		Last Modified: Tue, 17 Mar 2026 02:07:07 GMT  
		Size: 33.0 MB (32971122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:daf94dfb08c2b86e23fd38fbbc2bfcba22f4ddd6e8eb0db45d3d14e9bf929c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15903308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83f087973d0dee763ff1eef10bcddcaf859412d5a57a5299f66125b094f113a`

```dockerfile
```

-	Layers:
	-	`sha256:7d9afc4f316a671e2271015892e2f7b9985686559f66d5bd931fc3a500704d84`  
		Last Modified: Tue, 17 Mar 2026 02:07:07 GMT  
		Size: 15.9 MB (15884773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18178a58a43592232eacd5c1ca4f41229f9a847cfd91935373910d7fe0cd5e`  
		Last Modified: Tue, 17 Mar 2026 02:07:06 GMT  
		Size: 18.5 KB (18535 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:118453f266f42bb03032f427f4cc9205074d97aeea5b37d401b751c38d05c2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.4 MB (370408320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1062fcf4e34b79bc0409abe5474440b424741db5400f5a9d51e2b666b54105`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:08:53 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:08:53 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:08:53 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 17 Mar 2026 02:08:53 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux64.tar.bz2'; 			sha256='d560f4043180b0df5826396af17d060bd731e4fee34755167040924ece876f3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-aarch64.tar.bz2'; 			sha256='8aaed1e612e6874235ee9d5bd545a8dcc7b86c867d305351df37969390b0c47b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux32.tar.bz2'; 			sha256='14cb624e60b3012b4e5605571ab1477cea732a04e1c1385cc492d99f427a477f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 17 Mar 2026 02:08:53 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8feb033ce1635588aeb9a2f147293a6c61823ffee25286cf2fe9a0da9e069c`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 203.1 MB (203069864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2a237115f9828cc0ce26558d874461963eefe9311e953d75d5ef9553f5ba08`  
		Last Modified: Tue, 17 Mar 2026 02:09:15 GMT  
		Size: 30.9 MB (30881281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:928e7deaf5469747a3ad93bb773e76cb431e5d5c42f3ae18e141a969aeb1439c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15932034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef058e78e2a8d4560354cbbab0bd0f86fac3a58b64e1cc74dfbd388ff1d392b`

```dockerfile
```

-	Layers:
	-	`sha256:470306131f1d8cfdb7455c21ba8f2b1c8faf91ba0f13b3f9425ec376c0795130`  
		Last Modified: Tue, 17 Mar 2026 02:09:14 GMT  
		Size: 15.9 MB (15913347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175c7427ba0bceaec45fc5abcdb485118ee6c742c440c14a59bb28dd3805cff0`  
		Last Modified: Tue, 17 Mar 2026 02:09:13 GMT  
		Size: 18.7 KB (18687 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:d85f8d04d41d9b88b0810db366c889d08bace07bc448014c3d63f313f4547d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379587810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e2ad5293ec033a8272474c09b46462a1491fb2d471c68780c5b91b11d235bd`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:28:19 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:28:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:28:19 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 17 Mar 2026 01:28:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux64.tar.bz2'; 			sha256='d560f4043180b0df5826396af17d060bd731e4fee34755167040924ece876f3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-aarch64.tar.bz2'; 			sha256='8aaed1e612e6874235ee9d5bd545a8dcc7b86c867d305351df37969390b0c47b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.21-linux32.tar.bz2'; 			sha256='14cb624e60b3012b4e5605571ab1477cea732a04e1c1385cc492d99f427a477f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 17 Mar 2026 01:28:19 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28332827a450f227b37bf43cea8589364d96cbbc006b009e7d22789f013ded4`  
		Last Modified: Tue, 17 Mar 2026 00:20:17 GMT  
		Size: 210.5 MB (210473623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327a56020509e951e66a8a22371aa7ced48bda5b043fb8abab8cbbcfc3f5bcd`  
		Last Modified: Tue, 17 Mar 2026 01:28:37 GMT  
		Size: 28.5 MB (28530234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:575fddd3df17c717b0ab1f1a38a3f19758fcd23e2f92c03a53f57750eb3bfd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15881452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24dd5c7361c64e65d5f72ff43d1866f6e2bd7e54f0429ebe5b8cf209571c981`

```dockerfile
```

-	Layers:
	-	`sha256:5ff9528e891f121e498833d0340aced974dd0be5f8f17a3c7337a388511ec4a6`  
		Last Modified: Tue, 17 Mar 2026 01:28:36 GMT  
		Size: 15.9 MB (15862969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538dc3d373b288e80015dc8a9d0fbb2378b123a88bc756dd4e698dd3d7e8b543`  
		Last Modified: Tue, 17 Mar 2026 01:28:35 GMT  
		Size: 18.5 KB (18483 bytes)  
		MIME: application/vnd.in-toto+json
