## `hylang:0-python3.10-buster`

```console
$ docker pull hylang@sha256:4ea550e4cd4ad18f1f63d01b25f9c97bb3e15ea1417d33b223ea4608d6fe17d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-python3.10-buster` - linux; amd64

```console
$ docker pull hylang@sha256:738505aac9184e14ac7c04a22dd2e19df6dcdd6093955a24dfcb304b34c06d98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48858024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dce5fe82c62721a8b1b9d94e7972c4823bc7f15545231fb246549b63a4a2e13`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 04:56:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 04:56:03 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 04:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 05:16:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 05:32:38 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 05:38:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 09 Feb 2023 05:38:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 05:38:13 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 05:38:13 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 05:38:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 05:38:13 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 05:38:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 05:38:25 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 15:27:16 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 15:27:16 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 15:27:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 15:27:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c59e55cfd719490e5070eb007a3b0ffde33d3e36171a573a3224a050c1e341d`  
		Last Modified: Thu, 09 Feb 2023 06:05:47 GMT  
		Size: 2.8 MB (2781040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b58298de0d8fc8f69c675c463afab2beb87c60a81d13b5620c6b87ee42cbb`  
		Last Modified: Thu, 09 Feb 2023 06:07:00 GMT  
		Size: 11.5 MB (11470501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6239e464c1ab2cca0154db8e88c6b2eb8969c76dd4cdf8e67e03be54df84ac33`  
		Last Modified: Thu, 09 Feb 2023 06:06:58 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047dd5665bb1efccfca5ee9b67835b9accb753c462f1d531d62ea0c78923420f`  
		Last Modified: Thu, 09 Feb 2023 06:06:59 GMT  
		Size: 3.3 MB (3345476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88543ef7376cd24b4dd8d658b0d78bc44468248c8abba56c6de27028842122af`  
		Last Modified: Thu, 09 Feb 2023 15:35:46 GMT  
		Size: 4.1 MB (4120244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.10-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:61fd6f560d34fd1814db36c2e807623268095279cffd488989e0379df045deba
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43345536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63643d9b7e95be30d6e7774c5b6e3558526c750d3bdb42109548b2cd0fba25e7`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:44 GMT
ADD file:a8ec6525d364d668c197a3a8a8122778806534f0c87fa3282ea2ce6529c397fc in / 
# Thu, 09 Feb 2023 06:12:45 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:50:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 10:50:12 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 10:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:28:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 11:57:05 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 12:06:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 09 Feb 2023 12:06:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 12:06:19 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 12:06:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 12:06:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 12:06:20 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 12:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 12:06:37 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 21:35:46 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 21:35:46 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 21:35:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 21:35:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af790c31932b6069892469d33f363a5c03459bd259d72ae9e08431e6419ae97e`  
		Last Modified: Thu, 09 Feb 2023 06:20:10 GMT  
		Size: 22.7 MB (22749083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4152b00db0dd0a95cdf3a5b0bd1c507f0702cba034b989992630182b352dd1`  
		Last Modified: Thu, 09 Feb 2023 12:47:59 GMT  
		Size: 2.4 MB (2368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d60fbf7beeccfce1140bfa7e9e9fd1531ea0375aeaddd7e3527f1a00440c7ee`  
		Last Modified: Thu, 09 Feb 2023 12:49:48 GMT  
		Size: 10.8 MB (10765394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0649c21d702bda8560e3270d1c96bf93f156d1c11460957cfc1b8cff175e48b`  
		Last Modified: Thu, 09 Feb 2023 12:49:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0356e151afc08b362d81040b8aeaffdf44ffc12d81752da88657c424868f7981`  
		Last Modified: Thu, 09 Feb 2023 12:49:47 GMT  
		Size: 3.3 MB (3344512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb4a987b8bca9d6444729209de9a9832dc5c131771e83742dc66ec93afef43`  
		Last Modified: Thu, 09 Feb 2023 21:46:22 GMT  
		Size: 4.1 MB (4117917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.10-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4495fdaa267966e91aa5f5b172eafa2eff837a7142517fb35ce666998248ceaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47553540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855c2d6649eef0bb9ce056bb579a372d9064902858408a5964f56e08383360ea`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:02:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 07:02:05 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 07:02:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:23:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 07:40:21 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 07:45:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 09 Feb 2023 07:45:56 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 07:45:56 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 07:45:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 07:45:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 07:45:56 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 07:46:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 07:46:06 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 16:32:10 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 16:32:10 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 16:32:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 16:32:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a182a3139fcfa13084ea46c489a237f9597b907ce61fc900f52877d5ea3bf2a`  
		Last Modified: Thu, 09 Feb 2023 08:09:50 GMT  
		Size: 2.6 MB (2646777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edfb9062ae604b4d0c27f539f4a05e159a8d3964960b323742cf7585cc05a01`  
		Last Modified: Thu, 09 Feb 2023 08:11:04 GMT  
		Size: 11.5 MB (11518517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024b8b8e96bc481f2ec78fbee17b754fdbe9568917bb3d634729d85a6b8e65`  
		Last Modified: Thu, 09 Feb 2023 08:11:03 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4e6152f792104d91a3a2189eba1e0d9c16c993955dbd8dfd23716d4745b12c`  
		Last Modified: Thu, 09 Feb 2023 08:11:03 GMT  
		Size: 3.3 MB (3344918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0829e3d9d1db4597d9ace8f7ce9489db889d0b2489835c0f7168c3f9b557f945`  
		Last Modified: Thu, 09 Feb 2023 16:40:19 GMT  
		Size: 4.1 MB (4120270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.10-buster` - linux; 386

```console
$ docker pull hylang@sha256:2875fb8520a7c70934517ac3b846463e73d9b4ade9bb4b7b8cf410bbf54cf5e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49413317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361f65245a19a223e47e5a2b011f4d60fb3503c9de67e32d29ce4321e9a9d815`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Feb 2023 05:13:20 GMT
ADD file:2d19c71df422a9624e6fb34d6f87307703e1eaa800067eb1c594dd2b1778980f in / 
# Thu, 09 Feb 2023 05:13:21 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 08:25:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 08:25:04 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 08:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 08:57:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 09:22:32 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 09:30:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 09 Feb 2023 09:30:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 09:30:54 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 09:30:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 09:30:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 09:30:57 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 09:31:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 09:31:11 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 20:20:28 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 20:20:28 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 20:20:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 20:20:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bacc4719e321895e65d456a3375ac7c1f594877d62056057ca20a3229ce824cd`  
		Last Modified: Thu, 09 Feb 2023 05:19:30 GMT  
		Size: 27.8 MB (27798198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b414d1040bbaf517f775df04f29afc9e905049c143b1d4b642cbf3ac690ed1a3`  
		Last Modified: Thu, 09 Feb 2023 10:05:09 GMT  
		Size: 2.8 MB (2788394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9913710580e13a53615ac4238fea8abd8f0176c73558083a53aaf6114b0bb3ab`  
		Last Modified: Thu, 09 Feb 2023 10:06:42 GMT  
		Size: 11.6 MB (11576562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334fefb9440843889524c51ad45a4804285064b5ba5ab44f96c6f6324f128d40`  
		Last Modified: Thu, 09 Feb 2023 10:06:40 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e61db6543199813993bf30a2dcb98aa6326726ef1417355a84efec16bb652e`  
		Last Modified: Thu, 09 Feb 2023 10:06:41 GMT  
		Size: 3.1 MB (3132217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6817bb22b4cd08647379f917f8d83944c4e02c95ed6dab7aedd41b6b6b3e9`  
		Last Modified: Thu, 09 Feb 2023 20:34:36 GMT  
		Size: 4.1 MB (4117714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
