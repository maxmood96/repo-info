## `pypy:slim-bookworm`

```console
$ docker pull pypy@sha256:72c145db757ba0b7cbb6fa4c106a44b70aaf8a1f268fa80453913d65128cca8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:1b5ef3cb42ced278282b7cd2c30655c4b8e8383a2becd3c5f4066612acdadf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69944913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdea4e5bf79d015cc367bd18fc58e1e73dbd29561124b68cd678543cb8a8dcd`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:32:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:32:03 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 30 Dec 2025 00:32:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 30 Dec 2025 00:32:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4aefe667f4b5b7a7debbae3c16ecca50ee8baf62f0822afcb383588f074ea7`  
		Last Modified: Tue, 30 Dec 2025 00:32:22 GMT  
		Size: 3.5 MB (3509686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefbde2327349791aa82d557a278903dee741e9f514e1445c6e3838ee50e9161`  
		Last Modified: Tue, 30 Dec 2025 00:32:25 GMT  
		Size: 38.2 MB (38206803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:689aaa862aa3eb199e7f46ae05843b999503f120ac0cb56d682a0b74db0d2cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2150c4391ab6437b653ab7ec1d6cac9a10e8badf3ff0d94317f292ee24bf0b6`

```dockerfile
```

-	Layers:
	-	`sha256:aec6080131b8d2d26cce1f378cb92bf1b08f674dc3649425fef38758b200440e`  
		Last Modified: Tue, 30 Dec 2025 01:40:53 GMT  
		Size: 2.6 MB (2611670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357ed2036f4f4c73dfe5e9e8b458644cda2ac0758d0bb35d6c21e79c74bc6f36`  
		Last Modified: Tue, 30 Dec 2025 01:40:54 GMT  
		Size: 22.0 KB (21957 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:4145cb9224294b485ded5777e2d8e09cf444f83069ec2bf415a573ae5a13ee41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67966091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f9f7999b837cffa91f2d8772ad9a7cccab4084fa868057c342f3daa66e3247`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:33:45 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:33:45 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 30 Dec 2025 00:33:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 30 Dec 2025 00:33:45 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4eb94d70d264267c4801f17cceae25fab3ff1f9fef2f7118105883c73c7730`  
		Last Modified: Tue, 30 Dec 2025 00:34:03 GMT  
		Size: 3.3 MB (3340654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defa6ed9260371cdb8c0e4a54649cf56e438ba758095e73aa79b19ff150ccdbc`  
		Last Modified: Tue, 30 Dec 2025 00:34:06 GMT  
		Size: 36.5 MB (36523227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:8f77a4cf7b21d7665b18a02732e1fd5aaf3df056af2da218a9f5ae376b3a770f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c60d091c3268c12075c77ecccda27b2003239def490a190b5c7d640ea5d3b2`

```dockerfile
```

-	Layers:
	-	`sha256:57a12b99dabcd7cfc12d229793640bf5cc6db4911fbe18231b6c67620da7a571`  
		Last Modified: Tue, 30 Dec 2025 01:40:58 GMT  
		Size: 2.6 MB (2611997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e6909a2df102ba295cac72c41270c53b33ccf1dd8bc8097c3b2f1802fd880f`  
		Last Modified: Tue, 30 Dec 2025 01:40:59 GMT  
		Size: 22.1 KB (22136 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:4c7c906cbeb518fe25b5066ada0b291db81afa997d77f234ba5bed16fd042b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67420100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0de2c108ce233776ba88e291e98af06546f310e32417c1cebe3a8e9d89c5d0`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:58:04 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:58:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:04 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 29 Dec 2025 23:58:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 29 Dec 2025 23:58:04 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdc3f39196e26fa487313e555f78a561ecf41b8a252002acd0c3692fc4da707`  
		Last Modified: Mon, 29 Dec 2025 23:58:21 GMT  
		Size: 3.5 MB (3511012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10d32553254a598e4d6fc5e93e7616486ab0dac2a65da5fd18f2573904b1aa`  
		Last Modified: Mon, 29 Dec 2025 23:58:24 GMT  
		Size: 34.7 MB (34699315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:b9ded46ec1445dbd6e55f574fd58e920aedf65f56f08258144df7f1f8e3a323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba57147120199c836a231838329b243c3f4eb8915d8fd6598d67ca3d90a0170`

```dockerfile
```

-	Layers:
	-	`sha256:a484fc3711d4b4af4a91c0f44ec308baba4648404bfe3e695048cf4f38b0b34c`  
		Last Modified: Tue, 30 Dec 2025 04:41:55 GMT  
		Size: 2.6 MB (2608808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8867cf3a0a96a17437e1e5d3d93392aabed249dd4bd7005f0220ed7ba2af0397`  
		Last Modified: Tue, 30 Dec 2025 04:41:56 GMT  
		Size: 21.9 KB (21898 bytes)  
		MIME: application/vnd.in-toto+json
