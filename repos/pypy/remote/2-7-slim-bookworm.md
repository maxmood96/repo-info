## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:91e88af684f4a9e67ee03f1db36e5b7858de246d6caa2bfc4244916c49afa3eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:a07540e54685a0f0e6ce662f772ce287a5b1e584fe139a3b19f902c941e006a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64936672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc6bf0d13159a8d038724391e5b0cf5e47223dae64d63a2724a781716781af8`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:57:41 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:57:41 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:57:41 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 01:57:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux64.tar.bz2'; 			sha256='7833be48244a6f4aa0720c6b98f151428291a52697da849ef6b3ca7d5bf45b96'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-aarch64.tar.bz2'; 			sha256='b0bec20c16b6ab2bd46bd4f5d6049b6070a22a53eaed437ee9ac36d842ceda74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux32.tar.bz2'; 			sha256='fa6499281775ec22f4742e9dd7b31c22b8fc6a700c1cf50aebc7ef24f61461c5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 01:57:41 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0f0e30b5eb2f94f1d72c75e60d14bd49cd44cc1711588b63bc57d1e14c6118`  
		Last Modified: Wed, 24 Jun 2026 01:57:52 GMT  
		Size: 3.5 MB (3511598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cd18cea1a37bced844e52092c8554e489af0976807d20b43cfeb474247e2af`  
		Last Modified: Wed, 24 Jun 2026 01:57:53 GMT  
		Size: 33.2 MB (33187435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:1f2afe36aab452e8920853170edbad4920d996b88907c30b8b6df505f4856038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8073c2e8da37eb03b2e8f5a438b2b0f016a3fd34b18c1e0374984e91020480b2`

```dockerfile
```

-	Layers:
	-	`sha256:a2c02dbf05a2a40287593ea01b2d65dd348d9a95dfc1d975261a5d545f55d689`  
		Last Modified: Wed, 24 Jun 2026 01:57:52 GMT  
		Size: 2.5 MB (2495551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95276619b09853724e80e854484ccc72a3a256e09212adc293c01c437a2e38a1`  
		Last Modified: Wed, 24 Jun 2026 01:57:52 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:00be372b3a428d52be11359cf51f067d8a73742d9f7300320e52660ad3538de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62567067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8b8253d2f2d5d0d4fd87613364f7ff682ab129cfe0daf9dffaa59f1facbd35`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:01:50 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:01:50 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:01:50 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 02:01:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux64.tar.bz2'; 			sha256='7833be48244a6f4aa0720c6b98f151428291a52697da849ef6b3ca7d5bf45b96'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-aarch64.tar.bz2'; 			sha256='b0bec20c16b6ab2bd46bd4f5d6049b6070a22a53eaed437ee9ac36d842ceda74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux32.tar.bz2'; 			sha256='fa6499281775ec22f4742e9dd7b31c22b8fc6a700c1cf50aebc7ef24f61461c5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 02:01:50 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1149985f248d55912d1ccfcd7124e13bae033f918e43ce762d27f8486e518889`  
		Last Modified: Wed, 24 Jun 2026 02:02:01 GMT  
		Size: 3.3 MB (3345014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf94ddfc2b5687d0d63384615478b939d666c404e40c907452ba042ea433b4`  
		Last Modified: Wed, 24 Jun 2026 02:02:02 GMT  
		Size: 31.1 MB (31099635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:87e53e88cbfa58f722cba58461c456029f6eb3c6d0c520c5534334f2011380f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2515190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa17f3bc514c5f4e76b68c03b928de1b58e7a3e067ee1cee7f85ef76fc22d396`

```dockerfile
```

-	Layers:
	-	`sha256:48ca03e8af805a6f1370ab92f3523686a016645ec468e4d6cc0ba7e532570748`  
		Last Modified: Wed, 24 Jun 2026 02:02:01 GMT  
		Size: 2.5 MB (2495856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:878abd205d36c436c27fbd2e65a96245912e192a867a9256a62f3fa09190a84a`  
		Last Modified: Wed, 24 Jun 2026 02:02:01 GMT  
		Size: 19.3 KB (19334 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:436fafe6f0e45b4e884094f3766a608d45a0dbeaa279d75f6f8fbb56788c49c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61534694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5cc6172b21e5ac38b8bc565c060cda115c379b2c7d74fb6fff035ca4cfa4c4`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:54:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:55:32 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:55:32 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:55:32 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 01:55:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux64.tar.bz2'; 			sha256='7833be48244a6f4aa0720c6b98f151428291a52697da849ef6b3ca7d5bf45b96'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-aarch64.tar.bz2'; 			sha256='b0bec20c16b6ab2bd46bd4f5d6049b6070a22a53eaed437ee9ac36d842ceda74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.23-linux32.tar.bz2'; 			sha256='fa6499281775ec22f4742e9dd7b31c22b8fc6a700c1cf50aebc7ef24f61461c5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 01:55:32 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:df519b11ac99d8e2d452cbd55f824e658d0b86f649745abaaf8cbe33e2736a30`  
		Last Modified: Wed, 24 Jun 2026 00:28:03 GMT  
		Size: 29.2 MB (29225809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6b14359a5ce5e17bfabeca279f54390ab71a99f19c48a9f1797345b56b896`  
		Last Modified: Wed, 24 Jun 2026 01:55:12 GMT  
		Size: 3.5 MB (3515695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b8acea29c05a9dddac5f277d55c7a936fd1f97f55a737ced5e725e5cf0806`  
		Last Modified: Wed, 24 Jun 2026 01:55:42 GMT  
		Size: 28.8 MB (28793190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:f2d812d3a482214d9701815b157552ea828e05ee12747f772ffe0854b503a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bba91d3b04f1cec9bdb5f4eabcbcb69355f70832511a3ee63f7c9f90ee5dd8`

```dockerfile
```

-	Layers:
	-	`sha256:a24083c65dd7ef65708d5fe34c74845a5742284af46db380d56a169a103ced06`  
		Last Modified: Wed, 24 Jun 2026 01:55:42 GMT  
		Size: 2.5 MB (2492714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:394700006216c7f249f1be8c74aadd703869b3562fd8b443c23bd1cf3ddd7ccd`  
		Last Modified: Wed, 24 Jun 2026 01:55:42 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json
