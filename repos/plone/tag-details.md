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
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5-python38`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5-python38` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5-python38` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2-python38`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2-python38` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2-python38` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2.14`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2.14` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2.14` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:5.2.14-python38`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5.2.14-python38` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5.2.14-python38` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:latest`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:latest` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:latest` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `plone:python38`

```console
$ docker pull plone@sha256:577ae7c2a1a1c9acb75473b131265ce93b804971eb841b82be1ba872534a8091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:python38` - linux; amd64

```console
$ docker pull plone@sha256:f5e688ac6393f18f681416ae0509811130b9a6a3c69e82cc2c73ed4231c9d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269075004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64923d0e47fcc024ca4db33b535a51690597afbe1489d290fb629a528d48dad6`
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
ENV PYTHON_VERSION=3.8.19
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 31 Jul 2024 10:13:39 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 31 Jul 2024 10:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a0f7cc5bed327320889974b219a47be9c65256d64e8f5b2884536771190b4069`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.1 MB (1076316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf67fcba1d0003a5f4eb28cd51da76e7c48d65d6a5b49207216a912bfc8c`  
		Last Modified: Wed, 04 Sep 2024 23:11:01 GMT  
		Size: 10.8 MB (10829121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6d42bc7b83b1a566aa315f8043ad058def1d471a46300a74b40332f84429e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dce14312ebf1552dc21a4ffa8f8e65f03e5c6ebf3d79a88b86ddc3e5c51258`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 2.8 MB (2775049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef328315b4becddacc504932a83607b27157f0ddd34f3c9310f8db4733b750`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 3.8 KB (3806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f08e51f0e6467411d6c62232432f85d52a0ad18ff1e01aca09b31641302f5`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ac66d884abfc9f240ef4309c94e6752b02364578e9c32cebf68de88ae71f`  
		Last Modified: Thu, 05 Sep 2024 00:40:34 GMT  
		Size: 223.0 MB (222956496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33b275624334a8006584e3c50e2bb4c8a26096c98674bdcb75ed0890872cfa`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:python38` - unknown; unknown

```console
$ docker pull plone@sha256:ad413bb0b2b35678e7d042f42770dc614c8ae6894ff9abff55c73de648f2caf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20d893000a9629dbeba35c4ee190f43b902c02726512d781c99fe512e2880b`

```dockerfile
```

-	Layers:
	-	`sha256:a990d7419ff38818255811fc9e946d02e1e2468dc59b0fc653dc082f35f3fafd`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 7.2 MB (7151101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae38cb2f1bf2fc2ac446843cdbcf4861967d6b83957f7508bae446352c4d244`  
		Last Modified: Thu, 05 Sep 2024 00:40:30 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json
