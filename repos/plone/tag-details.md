<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `plone`

-	[`plone:5`](#plone5)
-	[`plone:5-python38`](#plone5-python38)
-	[`plone:5.2`](#plone52)
-	[`plone:5.2-python38`](#plone52-python38)
-	[`plone:5.2.14`](#plone5214)
-	[`plone:5.2.14-python38`](#plone5214-python38)
-	[`plone:latest`](#plonelatest)
-	[`plone:python38`](#plonepython38)

## `plone:5`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5-python38`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5-python38` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5-python38` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2-python38`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2-python38` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2-python38` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2.14`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2.14` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2.14` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2.14-python38`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2.14-python38` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2.14-python38` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:latest`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:latest` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:latest` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:python38`

```console
$ docker pull plone@sha256:76cdc5a69bb8359e876552cfcf122fd7ced4c0f7dc3e75a80066b5177398a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:python38` - linux; amd64

```console
$ docker pull plone@sha256:f702e4621fe874873a0970cf7d9b707f4be76fddd8717823e568a99f5dc713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f05d3a5607d9b4625b1c54a38558a41b6d8ad7e868348b860b2745b07c64b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["bash"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jul 2024 10:13:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_VERSION=3.8.20
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["python3"]
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PIP=22.2.2 ZC_BUILDOUT=3.0.1 SETUPTOOLS=65.7.0 WHEEL=0.38.4 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.14 PLONE_VERSION_RELEASE=Plone-5.2.14-UnifiedInstaller-1.0 PLONE_MD5=e8e1f774f069026319be3038631e0734
# Wed, 31 Jul 2024 10:13:39 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
COPY buildout.cfg /plone/instance/ # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/* # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
VOLUME [/data]
# Wed, 31 Jul 2024 10:13:39 GMT
COPY docker-initialize.py docker-entrypoint.sh / # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jul 2024 10:13:39 GMT
WORKDIR /plone/instance
# Wed, 31 Jul 2024 10:13:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" "0s" '\x00'}
# Wed, 31 Jul 2024 10:13:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jul 2024 10:13:39 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ec07f6ea876c69a77672c6f15f65ae3f3a2ccdba45ce55b614ecd32cfe3cb`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 3.8 KB (3807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f187b7e29d26ff39b1c9f61493d7644a40902692caae4d8d5cb4d3653cc3c83`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae75896731cc471db8ab9de6acba4590f77872b9887178477e923e4e6205da6`  
		Last Modified: Thu, 12 Sep 2024 22:30:45 GMT  
		Size: 223.0 MB (222955595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bba8b02bef3dae69c44d9da1467acb3d534ac95a9237e92142b20aece71e6`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:python38` - unknown; unknown

```console
$ docker pull plone@sha256:f5246d47a3acc1697873b552a0151ac77e814d3ebd9672259e037a8b44ff7c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a285ead4acb0a03cd1aa662d275455b3dfeccc6db256d4565dbe6d722692752f`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f11cc5fa0c287987ae8ae36d485e496bbff56fb360ba5b2525ec52efdb6af`  
		Last Modified: Thu, 12 Sep 2024 22:30:40 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbe819bfe1bad7e124122b9447c13e0a2863ea710d6ff392f8d588264fdc75f`  
		Last Modified: Thu, 12 Sep 2024 22:30:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json
