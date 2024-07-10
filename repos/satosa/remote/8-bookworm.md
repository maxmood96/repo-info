## `satosa:8-bookworm`

```console
$ docker pull satosa@sha256:96a1736c7df36f6bbed0e3542c727f9d9416bd3fc4dc1e62f2ca0a70b7e96c1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `satosa:8-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:cce6b524ff6e2c32a21c7428eff13cbe6bd1c2b0f69bcefc711e074d53720fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89851325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357a1b98d42b45c93431e5ce95271075b55f14de80730a963ed68dc56b1b7599`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2856587ea65e3410ea3ada83efe0443cb8c8bb212c9c9743a97ecd6a9cc8037`  
		Last Modified: Wed, 10 Jul 2024 19:10:55 GMT  
		Size: 3.5 MB (3509907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633d497474f09f1192b35bf8d38ce4c193288341a85269bbe0de60646d441ff`  
		Last Modified: Wed, 10 Jul 2024 19:10:55 GMT  
		Size: 12.0 MB (12005910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49add4e87504fc07f027a844f3f65bce6b6bd7a84442c853070247e4cf8c9c9`  
		Last Modified: Wed, 10 Jul 2024 19:10:55 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a503d964c7603f1a5e6ab64aa6fc5afa9a13b0199abceeccc34a1f00649ad6f8`  
		Last Modified: Wed, 10 Jul 2024 19:10:55 GMT  
		Size: 2.9 MB (2875445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f92a05db6cb98a5bede9cbf29be28aa2555668619145cc381ecae04671a4cae`  
		Last Modified: Wed, 10 Jul 2024 19:55:58 GMT  
		Size: 21.9 MB (21938414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba38576176d82b31f326885850932858a583fd7c33adc219bcdcc85f94b3b00c`  
		Last Modified: Wed, 10 Jul 2024 19:55:58 GMT  
		Size: 20.4 MB (20383048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e8dec3b0cb4142afbd1302b431c0c347bb5b9ea2cd3bcf9979200060b7057`  
		Last Modified: Wed, 10 Jul 2024 19:55:58 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e41ee8f0e8c27ca304785308af8829a943dfa30386ca38a5345bb4f4af74ab2`  
		Last Modified: Wed, 10 Jul 2024 19:55:58 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:ddfe5124375f0f2c08dde63be1cbd24b21f6d43c0818dfbee43e128ae8ca4e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2587264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c061322be6fd69ed36dd4cc3a94a86f870c2e1346fc406e101e4e7638a1795aa`

```dockerfile
```

-	Layers:
	-	`sha256:25a287efd1db207edf01ebd1e3ae4557f12b5eac7dbc547ae52f073151fb3533`  
		Last Modified: Wed, 10 Jul 2024 19:55:58 GMT  
		Size: 2.6 MB (2563781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b410c77b661a85f9da82ab4124dc45de4d8c98c84cf7dc510601a09bc68b75`  
		Last Modified: Wed, 10 Jul 2024 19:55:58 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:db1a466bc8a034e3bb6e1fd0faabd318fd9e8739ad88b726581463894206d87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89002961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e2c5731d9928090ccef1ae31a388eb1d39dbd6a9ae4570a1bd318bb06400be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13e32d8cd0dd6045ae8e76baa59b01457fb37cef4627f2e033eba1d883a6f`  
		Last Modified: Tue, 02 Jul 2024 21:00:39 GMT  
		Size: 3.3 MB (3329912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee30644a5dcc1af1caabea58d40e7757b2b5e1a7a798ff4ee9569b04b4b8f11`  
		Last Modified: Tue, 02 Jul 2024 21:00:39 GMT  
		Size: 12.0 MB (11977351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c7fa2607b2097467f2c1af3017121be58be80cdee4c1e9fbbe578b5308db04`  
		Last Modified: Wed, 03 Jul 2024 05:22:03 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a722882a2fdcc8fbef19a4eb7c9b0a4cd3d4c5ee0bc68dfdc071c90f1aa86ed8`  
		Last Modified: Wed, 10 Jul 2024 19:06:30 GMT  
		Size: 2.9 MB (2875632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b799283c497ea24f881a4c263a9a643db91da845fcbd262f43eb7db25905778`  
		Last Modified: Wed, 10 Jul 2024 19:56:10 GMT  
		Size: 21.8 MB (21780633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3c9cb96e433b7b1937a4d71fd45c84db3ba4f341c22099c76c1927bf282ca`  
		Last Modified: Wed, 10 Jul 2024 19:56:10 GMT  
		Size: 19.9 MB (19870554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c38528a7f639d0a5d294f9c7768ad97dd3ea6d3026c4f42a6c56111a294de61`  
		Last Modified: Wed, 10 Jul 2024 19:56:09 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7625292be826f657e60d12b13c5ff9d1c5f894c2fde08de8f4fbd0417615cf2a`  
		Last Modified: Wed, 10 Jul 2024 19:56:10 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:9ee6650af81b9c2cae7d530cc3ee671882a7b12f8a50ff4eebeaa8e591c4fa4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d8eb6c435dcb6fc6483b5cd84edab92a9b86fd34cca5027d5ac4fc6d64cbe9`

```dockerfile
```

-	Layers:
	-	`sha256:035799b27d0a76ce0d4fb3b4240a6d4a9e12f6e3f787182450be6e9eb319f52d`  
		Last Modified: Wed, 10 Jul 2024 19:56:10 GMT  
		Size: 2.6 MB (2564116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b61f8e086cf6e2ca4814def4bcc981918f155f57ef66aecbefdbd60d01b9c8b`  
		Last Modified: Wed, 10 Jul 2024 19:56:09 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; 386

```console
$ docker pull satosa@sha256:e40ed169d885ca99b710f359c41882e48eb20fe4d2830666b9e6e5055c35fab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385720657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c0914981c80230461b89e7f603ff53299fa4d93165d5c2604fbf5c664eb0b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961a27612ec75e71bfb466c8e820c5679aabdbe238ff8ef85c0f9a6a1a982fb9`  
		Last Modified: Wed, 10 Jul 2024 19:12:57 GMT  
		Size: 3.5 MB (3507310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be646db71d1217ec924bd3962f14e606e818fe8d42a6ac10755d7b9a271e4f6e`  
		Last Modified: Wed, 10 Jul 2024 19:12:58 GMT  
		Size: 12.3 MB (12252870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08f42d391ed6361922023ac9409bd8289b964c65898910051bb0499fad436c4`  
		Last Modified: Wed, 10 Jul 2024 19:12:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fbb3eea0c062e9613757dac9406c5379911b18e8917788025668fbd2e19f6b`  
		Last Modified: Wed, 10 Jul 2024 19:12:57 GMT  
		Size: 2.9 MB (2874969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba19630dee07e529708cb7072e20a8909d482c07518d54f3c0b8249dd3caecb8`  
		Last Modified: Wed, 10 Jul 2024 20:00:12 GMT  
		Size: 24.2 MB (24184863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390559ba964286e49ac5631e9c9f484ee95b7e49b003799504c26d59aa0fdf4`  
		Last Modified: Wed, 10 Jul 2024 20:00:18 GMT  
		Size: 312.7 MB (312744049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab79fd15ef0d5a48e4dfcda9e2f2b9601f8af9126b0de4193953978004ad4a0`  
		Last Modified: Wed, 10 Jul 2024 20:00:11 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f67c404df6456edbe83f79c849730c9c133bbca70cb4a5e117aee84d3d7d2f2`  
		Last Modified: Wed, 10 Jul 2024 20:00:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:ab2a0c821fdb925fb71a1a45c4c885d3bd61686edf32d460a961e9b9b762cdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd2f73f00eab95fe9605c6f7412cf6e66f522be73f0ef4a97e12a00c0dff4d1`

```dockerfile
```

-	Layers:
	-	`sha256:eb7dbf1906d89b2401b7e993cadd3085356d52319544e753f53974f68e63e85a`  
		Last Modified: Wed, 10 Jul 2024 20:00:11 GMT  
		Size: 2.6 MB (2560822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:871e36638e011b74c8f5f809abb5f6dde87b9cfafe52df70ba9a3445511cd258`  
		Last Modified: Wed, 10 Jul 2024 20:00:11 GMT  
		Size: 23.4 KB (23430 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; ppc64le

```console
$ docker pull satosa@sha256:f64987e426cc0c421f5a25612d168974a12b1c48cdfb3bd555ebe4effa457129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369937885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4007b9897017eac11cb5d83c61220e7f77364f2f2163ed1c466d67260bb270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f6c403ccc850ef15c20429df36acc7fe9ed45bf9d7766b1396d833c57a4df`  
		Last Modified: Wed, 03 Jul 2024 12:23:24 GMT  
		Size: 3.7 MB (3708161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722378d30b8652f344ea6bdac3e8eedb5d49a49051815d53db6206c360116047`  
		Last Modified: Wed, 03 Jul 2024 12:23:24 GMT  
		Size: 12.6 MB (12616759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dca1fa3a5217c87ef57898b9cacd4e282ea56ae77ffbfc92c25809394b57cf`  
		Last Modified: Wed, 03 Jul 2024 12:23:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6b4f60ce3c93981150d71f4db19dd8ccee2edfcec7b82f09a705f725c4b169`  
		Last Modified: Wed, 03 Jul 2024 12:23:24 GMT  
		Size: 2.9 MB (2875549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216506bc90d9ef56b830a0b0a41a6f125a47f81300f6145c636917cbab6ae4b`  
		Last Modified: Wed, 03 Jul 2024 22:55:07 GMT  
		Size: 24.5 MB (24463070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb4892d06d7ae78f6a7a51b1012a9ded6087522184ff4255364d14b2e8167fe`  
		Last Modified: Wed, 03 Jul 2024 22:55:22 GMT  
		Size: 293.1 MB (293139746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84705afca8879cf87aad32589caa583d77fcaab7974c9bddc6f80147694314b`  
		Last Modified: Wed, 03 Jul 2024 22:55:05 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c3c353a8ed44e11a82557b7536488b7f23747f4e380d31e7a1a76f1c1982e`  
		Last Modified: Wed, 03 Jul 2024 22:55:06 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:fc562a34250d7c70f6170aa3d93aaf7ab985b4c92e32105d88934213d9e6d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c448ccffc900604fbe4bec92a7f5e5f80eb90799e73c5cf4effd1dcbf01995`

```dockerfile
```

-	Layers:
	-	`sha256:a28dbc4d4aba3380c8283093276da13f336b472e692e0db304a22cd30076f711`  
		Last Modified: Wed, 03 Jul 2024 22:55:06 GMT  
		Size: 2.6 MB (2568287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dd5c1dd00174f94496c754e47add3b457e03c4129b0909e4aca0b055cb006c0`  
		Last Modified: Wed, 03 Jul 2024 22:55:05 GMT  
		Size: 23.6 KB (23595 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; s390x

```console
$ docker pull satosa@sha256:8021f764c72178c69a57af36fef3c2b22aee94827e6f41d4a7c58fb92698a042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383423148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f48d85d12fd30c3e626c4245362721f4d2c621f7256fa3a0e3c45b130d0179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bf27c1e85db88a8895753d07df07ce2736432c228a810e199a590621a5aa3`  
		Last Modified: Tue, 02 Jul 2024 09:12:22 GMT  
		Size: 3.2 MB (3170396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8a2f462ee86d0ca25278896a3b5aa11dc88c15c463b635fe620e878556ca1`  
		Last Modified: Tue, 02 Jul 2024 09:12:23 GMT  
		Size: 11.9 MB (11935323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e40fff8d4f170cd21eb083b833e1740f9372fee24f7fb65b3ca553637ffc8a`  
		Last Modified: Tue, 02 Jul 2024 09:12:22 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27b61f84ff917c05a67ad95f1c3430b55233626dbcb74b4632f9883b782b5ed`  
		Last Modified: Wed, 10 Jul 2024 19:08:44 GMT  
		Size: 2.9 MB (2875192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5448c4dba0156cc2794302145aabd533c995983c6dbc8938eef5d7b2aa057dae`  
		Last Modified: Wed, 10 Jul 2024 20:02:13 GMT  
		Size: 23.8 MB (23763472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a052d6c415ea1df076447e1b893dad100b4592e952a4e5bec52a34ed119c11`  
		Last Modified: Wed, 10 Jul 2024 20:02:20 GMT  
		Size: 314.2 MB (314176353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2eed0485d1af97781b12013c25955cfbb20ba8b68e85f2048dcbeb84f4a3ae`  
		Last Modified: Wed, 10 Jul 2024 20:02:12 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d2c196c625ad92248c87164d81fa94f32b3640530bbc49517484e33fb4e677`  
		Last Modified: Wed, 10 Jul 2024 20:02:13 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:bdf71d5588adf2f6ffd41dfe07c365f27411577a569e7652a8d56c99cff9c3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2587103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0be5b8c4a39b620b2cd4d5f13069a2a7a213c25810aca805dd6cb3a46f2e06f`

```dockerfile
```

-	Layers:
	-	`sha256:174444c2e747282535a1eccf7da761bc2f806f24135814fc6c6c7fc5a0c55743`  
		Last Modified: Wed, 10 Jul 2024 20:02:12 GMT  
		Size: 2.6 MB (2563581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a5b9c584e02d02a5e68e26975ff9b68a2ebab3bdd0bcbf7f4dfdf5e027031b`  
		Last Modified: Wed, 10 Jul 2024 20:02:12 GMT  
		Size: 23.5 KB (23522 bytes)  
		MIME: application/vnd.in-toto+json
