## `hylang:python3.11-bullseye`

```console
$ docker pull hylang@sha256:be2087e66345582902cae2964d9071c6b9a3cbc04cf7041e23d24bb05041b610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:python3.11-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:94730db3e09e9ae46ad321f7fc7363f6f8142b2946ed748ca488e5c3ae1eb958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59591078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17f1e7b746c064db8bca3109a8e38f293111838c7fb37d5b3d762ac0744d832`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55068ccf9224282903a479f338d13fc72a44d3b42f674924b92e1028d6275d4d`  
		Last Modified: Wed, 04 Jun 2025 17:16:33 GMT  
		Size: 1.1 MB (1077884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b381b85bdb85403d13e4a5857123a5964a905ac88c48e55b47f3294406600e`  
		Last Modified: Wed, 04 Jun 2025 17:16:38 GMT  
		Size: 22.0 MB (22048973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0589d429b7591699d6a64a2bf562b8cebf6ca9eba08810880407d7dd8f84699`  
		Last Modified: Wed, 04 Jun 2025 17:16:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4120c673739141ab6063b0b1d963c88061f1e7da6b5bdae071206fab1a4eb3b`  
		Last Modified: Wed, 04 Jun 2025 21:20:27 GMT  
		Size: 6.2 MB (6208032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c67c2a20f37f7b76db86954d161d32610c70cb4d0dbb85416bf70f7d965c9ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1417247f38f19a8cb0a363ed5d581cb604c535341da87b509eb6ee2d3eadc8d`

```dockerfile
```

-	Layers:
	-	`sha256:21264a01020128fd3fcffd63cb356dc771ec1e55ca2d979494901819163dc81c`  
		Last Modified: Wed, 04 Jun 2025 23:22:02 GMT  
		Size: 2.7 MB (2738999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8586ead032d1e96d6c18fd0f9f89f698fd9c327357cb70100341d4ac58302b65`  
		Last Modified: Wed, 04 Jun 2025 23:22:03 GMT  
		Size: 8.0 KB (8029 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:31e7909b688371712354b82bc28183adbfcded97352bff96c17a550c057870ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52515590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388c11e1ec15f1de7007b592000e3c72feae962ea6abb27080268fcf0cb2413f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d77e6172c26b4080a501eca67ca27311fbd0dabd85e4ad4d0387ce4631519c`  
		Last Modified: Tue, 03 Jun 2025 13:50:35 GMT  
		Size: 1.0 MB (1042868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835757658659a261221463e691189569ce9a01b5a8abeb01b266525dcc742e1`  
		Last Modified: Wed, 04 Jun 2025 21:31:15 GMT  
		Size: 19.7 MB (19720495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abda98d66a71876b4f6b19ad6ed9a10fec3bf059d656b21d833e3380109fb074`  
		Last Modified: Wed, 04 Jun 2025 21:31:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198fe98afb86b478fd744126b1203091c674d89288c221cbc41dc330337d499`  
		Last Modified: Thu, 05 Jun 2025 01:28:35 GMT  
		Size: 6.2 MB (6208075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:046a7165ccccfda17817d0deadfecbc9e719a0d265ce2de676d0f614414a3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185a821bca5a664b57ab2eae2f70d40825f6da3484308ab0e4485db04953aed9`

```dockerfile
```

-	Layers:
	-	`sha256:dbc92071d0ccadcd69ead287e65e82e4843a91c3b26ff470393a92bf3ca70827`  
		Last Modified: Thu, 05 Jun 2025 02:18:44 GMT  
		Size: 2.7 MB (2742840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e066931c41abbbd011cd036ebe74384ea9762ce545fad8f32a988f953b4669`  
		Last Modified: Thu, 05 Jun 2025 02:18:44 GMT  
		Size: 8.1 KB (8105 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c99a74095f20dd391507ac450e8a6c36dcdbabb92811d52df8b946bc944a98f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57189846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36741733a175af41c6286072ce2484f17137fae047e1fc5ac23d9ae579aeaf36`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f68d4647786cc15bd979e88aef7c4edf03f28557e1b55612599156bdb92f7f9`  
		Last Modified: Wed, 04 Jun 2025 19:02:33 GMT  
		Size: 1.1 MB (1065725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9416e7a8fc9d85eb8b6cd6057c64e266ac7e25525c9933bd0ced87a26e2556`  
		Last Modified: Wed, 04 Jun 2025 20:01:56 GMT  
		Size: 21.2 MB (21169645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c591728423616d54ba4dee3aa67fcaf79d5bd4533338e4e76bffd7654061383`  
		Last Modified: Wed, 04 Jun 2025 20:01:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cc4323b8aea37899ae5ed695cf40e48bd4b596aec38add80a31fcb1cebaf65`  
		Last Modified: Wed, 04 Jun 2025 21:52:21 GMT  
		Size: 6.2 MB (6207970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6ab735652552b0e8cb3c9ae31ea18f600004991a3b29444d9b0b761e3fc7edca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ca9d82c417b265a1e6d3b5953afeb7f1c82a6540028079b50013b2e8b53621`

```dockerfile
```

-	Layers:
	-	`sha256:9dd8fdeefeb4d05710dfcf43b05948688cac5b29f7d111062ff10414653f287d`  
		Last Modified: Wed, 04 Jun 2025 23:22:10 GMT  
		Size: 2.7 MB (2739258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df83fe654d95fda6486b7807c8e9b31c5b221bcc5c4285d53322e6e86d8581e`  
		Last Modified: Wed, 04 Jun 2025 23:22:11 GMT  
		Size: 8.1 KB (8133 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:8658a240322516ed26df033dce8d9c386290242c42123c66cf2837e5cf118c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60200069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b392af0cba892269422c4f714379549b90196562672670a17f6c2ef8c98395c3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a49379a1b53c2e82b21f71e2fb3b3c54cc006327f43438bdc16c81fdc6f72`  
		Last Modified: Wed, 04 Jun 2025 17:24:32 GMT  
		Size: 1.1 MB (1090557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3fffea5369d7f4a643abe76b8c4880f34b84af0d7a87b1a22eaa46b7c9c40a`  
		Last Modified: Wed, 04 Jun 2025 17:24:36 GMT  
		Size: 21.7 MB (21712054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9903b921be57f2948d26c6d9d28e93066a63f02d2caabfe0c20734dba4020bf`  
		Last Modified: Wed, 04 Jun 2025 17:24:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa00757843ced61ae8c837237fcd848f6c72f65ac9e0ce4ec4f93bf8b179e96`  
		Last Modified: Thu, 05 Jun 2025 02:05:36 GMT  
		Size: 6.2 MB (6208010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:ca3dd7622ee49be7d7705389c09aca23271d3b00a8ffbfc99d46ce4d63c17329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec961d9d9cfcea87dfbe423a914b6fa4cea39978aab9ac8d27af431114818aa6`

```dockerfile
```

-	Layers:
	-	`sha256:6e4381814a073d5ec451bc056d588d7e88c1ca96fef89c471705b1d785f82b80`  
		Last Modified: Wed, 04 Jun 2025 23:22:15 GMT  
		Size: 2.7 MB (2736162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67573ac8682cf5f4754af838cd9735c02e05214b6b1072d8554a13f32a3a6517`  
		Last Modified: Wed, 04 Jun 2025 23:22:16 GMT  
		Size: 8.0 KB (7997 bytes)  
		MIME: application/vnd.in-toto+json
