## `hylang:pypy3.10-bullseye`

```console
$ docker pull hylang@sha256:7cd8df0e2b6105f0acf1f66903536a6b31106af7e3372dd9dc6a5b5628f93bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:2bbe3cfe00869fb9b82200728fd23090b527b8cc72d1538a8dde7d69dc94b65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78778953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3b8a7f48c0c905b0307034075a3508cb51701ea6517272d38b59ed474da5b8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4f9f0fcf54f1814db430ec12ba2728bdae68ffeffccc1c97064b6a7eaab7be`  
		Last Modified: Tue, 19 Dec 2023 16:04:12 GMT  
		Size: 1.1 MB (1068495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973fa23353456eac5ff7425727c5dc38352776e97b88ce07cd1f0971e4c2800c`  
		Last Modified: Thu, 28 Dec 2023 01:37:35 GMT  
		Size: 36.5 MB (36458025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70178e82cf4ef17ab04d4fc5eb363fc09f0d64d69c33b4ae6bb358b39d431da4`  
		Last Modified: Thu, 28 Dec 2023 01:37:30 GMT  
		Size: 3.5 MB (3519021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb4d54529e5b30536d47be6a1b7fe95f7df7bd8752e93f8d7cb2fee84649a68`  
		Last Modified: Thu, 28 Dec 2023 02:48:40 GMT  
		Size: 6.3 MB (6315539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:fe14865c4549fa23b56150ea6666bac9c604c71035b67977c7e413d1910ae956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8561e5864db7a41eace0f33a0d24536eb970eeaccbbcb523572177606b06e62`

```dockerfile
```

-	Layers:
	-	`sha256:8010b8ac94bdf90e6cd8fed778dd7019693b9b917b4629f32dc9de9ffd276a26`  
		Last Modified: Thu, 28 Dec 2023 02:48:40 GMT  
		Size: 3.2 MB (3233591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f10d532fd54cd0cf40f93ea5950d10ebdff8ba36162f4c773f6cfbec002c12`  
		Last Modified: Thu, 28 Dec 2023 02:48:39 GMT  
		Size: 9.8 KB (9792 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ebce7859a4bec15f8c6cd879ae07f28d8acd9a4aada99d34c14c2cb8e7818450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75032400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9efebfecd7fd996c733c84ad882583f94692c1def87daa437fdb1850fdc8ec0`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca9389b369bc4c9568e2e93447fc474736aea2c14ad836e987f603c64f0cacd`  
		Last Modified: Tue, 19 Dec 2023 09:39:53 GMT  
		Size: 1.1 MB (1055771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da03c9ce872c6935bbb1006703ad2ea4dbca19a681f0411e28ee524dd01be6`  
		Last Modified: Thu, 28 Dec 2023 00:52:19 GMT  
		Size: 34.1 MB (34078242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5263aa162bc6cdf9944296a436d09995076c76dfdbc2345d535b00ec914db902`  
		Last Modified: Thu, 28 Dec 2023 00:52:15 GMT  
		Size: 3.5 MB (3518589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9a53b679690a613cd597af4380488973000d1fe9e39ccf991ea548973d3a1d`  
		Last Modified: Thu, 28 Dec 2023 06:21:54 GMT  
		Size: 6.3 MB (6315746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:feb10881c3db198c69f256510293d20da604f49580087aa254baa1f5a391bc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3221323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fee41a6cc6d8cf6bf2a32ae85e87ef54675bd589ef170ee90cd04d2301887f0`

```dockerfile
```

-	Layers:
	-	`sha256:8199988926bb7d8ebf76f0e52b948abc94423fde819a3d0a1af9bdb9a1af323b`  
		Last Modified: Thu, 28 Dec 2023 06:21:54 GMT  
		Size: 3.2 MB (3211515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79fbdb2c0d44305eefef7819efc6a1a7612e114087831693887d198bbeda533b`  
		Last Modified: Thu, 28 Dec 2023 06:21:54 GMT  
		Size: 9.8 KB (9808 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:85ad1500a9227d8cd7c8af4d644c36c14027c3a8e739a821c33826a19024bb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77273884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72163a00148a99fc14f014ecaaf6ec3409851f8e0901f315e3211f1005d3a099`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-linux64.tar.bz2'; 			sha256='54936eeafd9350a5ea0375b036272a260871b9bca82e1b0bb3201deea9f5a442'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-aarch64.tar.bz2'; 			sha256='ac476f01c9653358404f2e4b52f62307b2f64ccdb8c96dadcbfe355824d81a63'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-linux32.tar.bz2'; 			sha256='bfba57eb1f859dd0ad0d6fe841bb12e1256f1f023c7fbca083b536cccbc1233b'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.13-s390x.tar.bz2'; 			sha256='3c813c7efa6a026b281313b299c186c585155fc164c7538e65d41efdabff87c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7367da1b8eab9cfea04aa08f86bcc41a47320a602a6c5877d39f9f4fa6a4fb`  
		Last Modified: Tue, 19 Dec 2023 23:57:41 GMT  
		Size: 1.1 MB (1080425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e286d0938090ad7c98e2ec85e053e05cb2ab628b32f8c9fa33957de58cb01a1`  
		Last Modified: Tue, 19 Dec 2023 23:57:49 GMT  
		Size: 34.0 MB (33956875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1f4531a2e0b27fde3e25984b458875940f09b70cb1f03a4680e4a3563fe`  
		Last Modified: Tue, 19 Dec 2023 23:57:42 GMT  
		Size: 3.5 MB (3518538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defa7321f58b36f327cc3b71ded66bcdda3ad1b5fbe7dfaca53e181e191127da`  
		Last Modified: Wed, 20 Dec 2023 20:12:07 GMT  
		Size: 6.3 MB (6315358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3dd86e84892abbb02b6a11d432a8f7b6f0112d2d4963ed6f6643b60c8c65b37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb5bac74d8a82e07922e65e7dbbc93c6f96d6899a72ba5418d0500ed36b00d2`

```dockerfile
```

-	Layers:
	-	`sha256:b56582d203311a21283cd866c0a875749081a07292ec7516b7a336bdbb0a7be2`  
		Last Modified: Wed, 20 Dec 2023 20:12:07 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.in-toto+json
