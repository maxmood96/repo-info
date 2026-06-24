## `pypy:2-slim`

```console
$ docker pull pypy@sha256:638eae9e12c295d94a0af6575807a306fb33e7c9f26d71cdc68babb4c3a019ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim` - linux; amd64

```console
$ docker pull pypy@sha256:1049a0bfe0851cadf39f851785b2e8db80b7cb93309187085ddd0c7c7a3ebb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64188234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901e7382ff8fc6dc5fa5758a3df94e9568636843a78bd80902896478fa55c325`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:57:24 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:57:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:57:24 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 01:57:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux64.tar.bz2'; 			sha256='7833be48244a6f4aa0720c6b98f151428291a52697da849ef6b3ca7d5bf45b96'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-aarch64.tar.bz2'; 			sha256='b0bec20c16b6ab2bd46bd4f5d6049b6070a22a53eaed437ee9ac36d842ceda74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux32.tar.bz2'; 			sha256='fa6499281775ec22f4742e9dd7b31c22b8fc6a700c1cf50aebc7ef24f61461c5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 01:57:24 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b541b8c384ae1173755350f2107f7f309883f9ccdb68ccd61cc1e015b9b5a7b`  
		Last Modified: Wed, 24 Jun 2026 01:57:35 GMT  
		Size: 1.2 MB (1220907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb1d29eeb76839afaf56638932b325c0a17a3595dfb1e15915fc207b45f72a`  
		Last Modified: Wed, 24 Jun 2026 01:57:36 GMT  
		Size: 33.2 MB (33181908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:1f402794a783cea46e1ce6b1b55f5017d1b1b708d3879761c018026366687e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129ab3a79d278cd3cd844ac1d146c4bcefebc616c2d1b264eb2b9c8902b5093b`

```dockerfile
```

-	Layers:
	-	`sha256:152d5be6b6071873206acf9279668f8eb5e2f8912751fce2f0e6de837507d51a`  
		Last Modified: Wed, 24 Jun 2026 01:57:35 GMT  
		Size: 2.1 MB (2109347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47d95100bd2da1b958c22950c2334b92d4e868218a4d5d350187cb054f45f41`  
		Last Modified: Wed, 24 Jun 2026 01:57:35 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:afb1c6061331c55315778d2ded38fdc9c6ddc949dce84b84e9b81be65769a5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62446535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c61eca12701964fc3732e8c3bbbf80fb0f65fe35f688ccf4b103fbad90fb9f7`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:01:49 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:01:49 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:01:49 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 02:01:49 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux64.tar.bz2'; 			sha256='7833be48244a6f4aa0720c6b98f151428291a52697da849ef6b3ca7d5bf45b96'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-aarch64.tar.bz2'; 			sha256='b0bec20c16b6ab2bd46bd4f5d6049b6070a22a53eaed437ee9ac36d842ceda74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux32.tar.bz2'; 			sha256='fa6499281775ec22f4742e9dd7b31c22b8fc6a700c1cf50aebc7ef24f61461c5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 02:01:49 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8e649478afd149031c6935b9287a31dbce3744010b6fc9744fa4e9285fc9a9`  
		Last Modified: Wed, 24 Jun 2026 02:02:00 GMT  
		Size: 1.2 MB (1202543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dffde9cef014e03ec9eaaca7d58973c16925333f30d6305b60cbec644399de5`  
		Last Modified: Wed, 24 Jun 2026 02:02:01 GMT  
		Size: 31.1 MB (31095441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:10c70219e12fb815d7d56b18be49a814b6effbbd160bfd6e56c907446611e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f2ac4bc60967435c014aa21ddb77b65a718283cea3b28354eab847df012a9`

```dockerfile
```

-	Layers:
	-	`sha256:500346accc1bc8d48268c32b430c58f4911e0e6df96df1e1cca94b25ce1878fa`  
		Last Modified: Wed, 24 Jun 2026 02:02:00 GMT  
		Size: 2.1 MB (2109741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adf646786bea342ac4285ab8bd7347a5cad11bbb8bb70cd7747060a2dc3e7291`  
		Last Modified: Wed, 24 Jun 2026 02:02:00 GMT  
		Size: 21.8 KB (21812 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; 386

```console
$ docker pull pypy@sha256:7e6f494bfd2c73fb3afb5bec20100914bef17cfaea3ef4443656b7c4deccf3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61317769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec198db694611c728be29ef1381f3d61bdab61d68e7d1fd36e88a90e6684a6a`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:55:34 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:55:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:55:34 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 01:55:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux64.tar.bz2'; 			sha256='7833be48244a6f4aa0720c6b98f151428291a52697da849ef6b3ca7d5bf45b96'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-aarch64.tar.bz2'; 			sha256='b0bec20c16b6ab2bd46bd4f5d6049b6070a22a53eaed437ee9ac36d842ceda74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux32.tar.bz2'; 			sha256='fa6499281775ec22f4742e9dd7b31c22b8fc6a700c1cf50aebc7ef24f61461c5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 01:55:34 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6126effe8006a3677f61c37bd5131f3e0a0447c0f3c8c787d947e3d3d9c1c32`  
		Last Modified: Wed, 24 Jun 2026 01:55:09 GMT  
		Size: 1.2 MB (1228277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33deb63d4b5a5fbaa98bcb5d420d483417f517ad44be08ddbb43c49d5cdefafd`  
		Last Modified: Wed, 24 Jun 2026 01:55:45 GMT  
		Size: 28.8 MB (28788282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:a3f6c4034c8fede129fa171773d6be30b3fb6a0bfb67e5caa0539079d54e7e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2127939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88c89bfd21b2781a8ad1cae592e4e16a90c35339a6a9ea992fa8de644e2c1a9`

```dockerfile
```

-	Layers:
	-	`sha256:2628b7258830b08a0a304f63d65b6a3cba6f376ee48e4e9d75f3fbd8ea32a305`  
		Last Modified: Wed, 24 Jun 2026 01:55:44 GMT  
		Size: 2.1 MB (2106484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6748e3bd6f8f88eef8c19d89eef903267b5d7f0f722f0d5632bdabac1dfda25`  
		Last Modified: Wed, 24 Jun 2026 01:55:44 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json
