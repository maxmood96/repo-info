## `hylang:0-pypy3.10`

```console
$ docker pull hylang@sha256:5bbbdd529f3b590aa0153975a28cc3fe906555895e95b0f5722615700ad38df6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.10` - linux; amd64

```console
$ docker pull hylang@sha256:c60afdeb90ad8e1f9efef90264685ca24c5f6e944129976ff9da36e0aa602b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (79049368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bf41c62ad3e87f8ecf61968b2b9cebb4651c29abc8181c114a385c8c5215db`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff55b4937d7aa2d781980e2823df563c8b6725594e7c2af1678737f2be03744`  
		Last Modified: Fri, 05 Jan 2024 18:54:34 GMT  
		Size: 3.5 MB (3490908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d72a05d694bbbfcf64e2c204be1a24e0bb7b6826265e6784561d6ff502ce185`  
		Last Modified: Fri, 05 Jan 2024 18:54:35 GMT  
		Size: 36.8 MB (36786164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4735ca704aa01417cb467f2c09067c4e5f9a6f7106c79decc03c6fa182f26b`  
		Last Modified: Fri, 05 Jan 2024 18:54:35 GMT  
		Size: 3.3 MB (3306768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbef5a6f6c5f81e7dae579ed3dfb60d6339be31d7c97550f2e9567fb8ffaee17`  
		Last Modified: Fri, 05 Jan 2024 23:56:14 GMT  
		Size: 6.3 MB (6339565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:fd6065d88c7b2f41f28d727f66debe045fa13f95de8b02ead4fff2eee1cd3101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547c73055d9306d54a9b4db44410ca4595c2dc5e81470a1babedfc2b226e701`

```dockerfile
```

-	Layers:
	-	`sha256:bab1fa3600d64f21ac9bb073555c1f40000eb8d964aaa514e7710a16b828ee04`  
		Last Modified: Fri, 05 Jan 2024 23:56:14 GMT  
		Size: 3.2 MB (3150166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c3658c94d70f3266c10010edc1a2398e1cff18d24ee8034a14bb75e43fc82c`  
		Last Modified: Fri, 05 Jan 2024 23:56:13 GMT  
		Size: 12.3 KB (12347 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3fc6982765de7daae16564625434faf2d88d000b4cdcee1d5cd3ecb9d6693033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76246936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7f0a275e8e4788e72e800112c9a86451fa1f629f905d8e6508271bbb03b5d7`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb02f81cf1a233cf6e9f8f67cc4fa31d6cefb6c5f38a406131d69b8a31640fa1`  
		Last Modified: Fri, 05 Jan 2024 19:26:12 GMT  
		Size: 3.3 MB (3314096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67ba68bc391dc267bd9aeeeeea74e22cedaf05977883223799e3f993673779`  
		Last Modified: Fri, 05 Jan 2024 19:26:13 GMT  
		Size: 34.1 MB (34129309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d94414df54ab394c6ed704f4243fb60c02dd0930756471cfc0f6e890bed4c0c`  
		Last Modified: Fri, 05 Jan 2024 19:26:11 GMT  
		Size: 3.3 MB (3306609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4d2faa965bfecbac4e50652250ec8d3022a1ceeaf42c55e8996e24a810ebc4`  
		Last Modified: Sat, 06 Jan 2024 00:44:12 GMT  
		Size: 6.3 MB (6339653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:f1315e486bd7f7a1bf1555020cae59e6c798a2e0cc97ca7abd622fa2cde27327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d958db499c4b8722256e76290d4c4d0c7455b5ff6e522cbae2378a3bd36b4a0e`

```dockerfile
```

-	Layers:
	-	`sha256:9933fb360698c7a59d031fb19b8b979ac8c0ce73780611f496d17d9f82d1181c`  
		Last Modified: Sat, 06 Jan 2024 00:44:12 GMT  
		Size: 3.1 MB (3125365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda5fa7dcea8a6f8ca917999e3a78c50d88250ed225982b3348c6334ded91c6d`  
		Last Modified: Sat, 06 Jan 2024 00:44:12 GMT  
		Size: 11.8 KB (11763 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10` - linux; 386

```console
$ docker pull hylang@sha256:febe6daa65c0488daf4b8656109769b99f6d68540e65501b4a812d4b1675ba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75900185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0c64c5f0b9f3bfeb3655df5985b129bedfd26c906cba69bdae1a7780a2ca46`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53018d9daf91ba12be1cf6c60a88893f37dc9d83f4696fbab4ff67ec34ce277`  
		Last Modified: Fri, 05 Jan 2024 18:54:38 GMT  
		Size: 3.5 MB (3496065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abddeff0a9c2a2d4b8736ecf63dc7557fed32f90c1858b69cb203b149e2fc63`  
		Last Modified: Fri, 05 Jan 2024 18:54:39 GMT  
		Size: 32.6 MB (32614324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88a8534657e950e677b5f6afa7616304226d64474226046677e51ee8f80001`  
		Last Modified: Fri, 05 Jan 2024 18:54:38 GMT  
		Size: 3.3 MB (3306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fec08a4bb6bb724a8487163c3f8285be4ccba1a3558201f00d0605259f146b`  
		Last Modified: Fri, 05 Jan 2024 23:56:10 GMT  
		Size: 6.3 MB (6339518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:93890f811c9bc3d53cbf4b2820a9fbfbb6b2b0221ccff5f4541107cc5e98911c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af296ad11f40f2f98900fb82a80cea1dc564e17213f29c649de5d50ec75d67c3`

```dockerfile
```

-	Layers:
	-	`sha256:9d464d8d0c74a7d6bdc377ea500291573be2029f91b8e66fc5b4f08e46944d8f`  
		Last Modified: Fri, 05 Jan 2024 23:56:10 GMT  
		Size: 3.1 MB (3144447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7a9c763dfbae2feb1ec03198e08f78d592f35da97f25ad271edd50694ff630`  
		Last Modified: Fri, 05 Jan 2024 23:56:10 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.in-toto+json
