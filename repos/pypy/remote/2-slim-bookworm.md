## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:9523b87764e845fc8ac15283182317116c73088893e4b1ba1b7262d87227192e
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
$ docker pull pypy@sha256:eb4c91b235a5302566a08f2f558b652e02ba81c834aeabf2d0b8555afac94065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64912833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15241b06a12df15a42c314f7c2febb73b8471f987aa6faf75a19a1c3acf9222c`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:39:39 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:39:39 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:39:39 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:39:39 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux64.tar.bz2'; 			sha256='c47a4030542cbd34d0cb673a0de1956c94c1ebe6c6b094f2ae6a167c55375f68'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-aarch64.tar.bz2'; 			sha256='49829ef97a36d50870b0a4a7d6d67c4817d98a0bbd936e7a86ac6ef615b07205'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux32.tar.bz2'; 			sha256='3512d44a9005b52611ad2d84e63c575c8b592fb1dd1a708a00f787b46e6ee07b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:39:39 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801d2f2e9c4fd760dd085bc6dd15c452196f1044baff69889ef8eea74a18ff09`  
		Last Modified: Tue, 19 May 2026 23:39:50 GMT  
		Size: 3.5 MB (3511450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ccdac0329df13f959c08d6055f4895fcb091d42208981a570eb9fe3e7684a6`  
		Last Modified: Tue, 19 May 2026 23:39:51 GMT  
		Size: 33.2 MB (33167840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:9f6aec1cd55a611d778484594bb7b299a41c33fb097052bb657155d4e0a7f559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cffa604e041e3575765c56267bebf40731ecf8617a54362ff1c5b0739fe1a5`

```dockerfile
```

-	Layers:
	-	`sha256:e597d34df60e534a04d15d52ef25d00c90390b3fef71d0db1a613aeff2ed4c28`  
		Last Modified: Tue, 19 May 2026 23:39:50 GMT  
		Size: 2.5 MB (2495533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afa1e6331e522cb1838b5c03d3cf7a59a353072ca61aebf80c4f62c63ea01e3e`  
		Last Modified: Tue, 19 May 2026 23:39:50 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:c92587be77119df8a135bb33c80c9fea11ce1a25f815bcac75bd189f6ff44241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62496567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b1a5dcbb31ad82b28e333ac1102228c8f1dc425f0d5a64616393764ddb2d0e`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:57 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:43:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:57 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:43:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux64.tar.bz2'; 			sha256='c47a4030542cbd34d0cb673a0de1956c94c1ebe6c6b094f2ae6a167c55375f68'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-aarch64.tar.bz2'; 			sha256='49829ef97a36d50870b0a4a7d6d67c4817d98a0bbd936e7a86ac6ef615b07205'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux32.tar.bz2'; 			sha256='3512d44a9005b52611ad2d84e63c575c8b592fb1dd1a708a00f787b46e6ee07b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:43:57 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59ca6d26433d93912b9d9cb63a8f1af624a2a2602089ceb2f9cda1929f6f17`  
		Last Modified: Tue, 19 May 2026 23:44:08 GMT  
		Size: 3.3 MB (3344267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108f012ca21675207749de50522322a47d409055669635a3ac057724bc3c8dc0`  
		Last Modified: Tue, 19 May 2026 23:44:09 GMT  
		Size: 31.0 MB (31037257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:1cf4bf6eb23b5b2d65f62f678cd498804c1bc0486f27e0ce3c2ff36bb824296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2515172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf320e28a2afc3f1aaea37f261d0f97953b04a241aca1e10a2b03fecfb76b4`

```dockerfile
```

-	Layers:
	-	`sha256:21b5413ebd2975739d22941216f03af68b327f5cf7107528b156c6b87ab615e3`  
		Last Modified: Tue, 19 May 2026 23:44:08 GMT  
		Size: 2.5 MB (2495838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4bb2c46c371bceb1bd5d494062ae9dc43daedf92533ace89d01442d6a3eb92`  
		Last Modified: Tue, 19 May 2026 23:44:08 GMT  
		Size: 19.3 KB (19334 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:1438a6417455a12f6554a84b70c3e4dd36b1d53a048e766c12400deead8522c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61451392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32530aceb3bca89ff26caa58a1c220120962986319802b2468af1daab36c5b21`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:34:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:35:05 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:35:05 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:35:05 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 19 May 2026 23:35:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux64.tar.bz2'; 			sha256='c47a4030542cbd34d0cb673a0de1956c94c1ebe6c6b094f2ae6a167c55375f68'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-aarch64.tar.bz2'; 			sha256='49829ef97a36d50870b0a4a7d6d67c4817d98a0bbd936e7a86ac6ef615b07205'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.22-linux32.tar.bz2'; 			sha256='3512d44a9005b52611ad2d84e63c575c8b592fb1dd1a708a00f787b46e6ee07b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 19 May 2026 23:35:05 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554f13a0b32bc40b3fa4c668fec4732362fa1b7f12212687cb497404ff552e94`  
		Last Modified: Tue, 19 May 2026 23:35:23 GMT  
		Size: 3.5 MB (3515431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fdbc82b0bae2afdc45c618c398d4ce65e427ea4cfe756b33b8ba3ce1b557f2`  
		Last Modified: Tue, 19 May 2026 23:35:27 GMT  
		Size: 28.7 MB (28717360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:bb3d1e5f9d4b0d81848466d18ed3706363c83274d9a91c8e1767e269126d80cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b56c255f4a7d606527afc6507727be24785c0ed3467d4dc558dad7439d3cff4`

```dockerfile
```

-	Layers:
	-	`sha256:d4e76686460a4bfb3955c2764de0d6387baa583f6570c243d06558463269f55d`  
		Last Modified: Tue, 19 May 2026 23:35:19 GMT  
		Size: 2.5 MB (2492696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7299017dbda05ca4a9359f9627c915a7951b7538d5e0a2991e3e168b82e3f76d`  
		Last Modified: Tue, 19 May 2026 23:35:19 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json
