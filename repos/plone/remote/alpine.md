## `plone:alpine`

```console
$ docker pull plone@sha256:6361bb1c912e774b469acda8a1843ee620d95714d0656aaf5a6865fe9fda1568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `plone:alpine` - linux; amd64

```console
$ docker pull plone@sha256:2b5168fc7f5164148b62718d6aaa7230cab8d7f5e3e4a948f305a6c18898bef2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136866500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8e5127c4e62ba864ce773be7acfc1250d5c9b5d3ecb73705df7d59cf48c3a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 14:03:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 14:39:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 11 Dec 2020 14:39:56 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 11 Dec 2020 14:39:57 GMT
ENV PYTHON_VERSION=3.8.6
# Fri, 11 Dec 2020 14:46:02 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 11 Dec 2020 14:46:03 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 15 Dec 2020 22:33:15 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 15 Dec 2020 22:33:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 15 Dec 2020 22:33:15 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 15 Dec 2020 22:33:21 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 15 Dec 2020 22:33:22 GMT
CMD ["python3"]
# Tue, 15 Dec 2020 23:07:17 GMT
ENV PIP=20.2.3 ZC_BUILDOUT=2.13.3 SETUPTOOLS=50.3.0 WHEEL=0.35.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.2 PLONE_VERSION_RELEASE=Plone-5.2.2-UnifiedInstaller PLONE_MD5=a603eddfd3abb0528f0861472ebac934
# Tue, 15 Dec 2020 23:07:17 GMT
LABEL plone=5.2.2 os=alpine os.version=3.12 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Tue, 15 Dec 2020 23:07:18 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Tue, 15 Dec 2020 23:07:19 GMT
COPY file:e1c551fc370867c153c440542b0f297049c860021da1d914d102da702cd4376a in /plone/instance/ 
# Tue, 15 Dec 2020 23:16:38 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Tue, 15 Dec 2020 23:16:39 GMT
VOLUME [/data]
# Tue, 15 Dec 2020 23:16:39 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Tue, 15 Dec 2020 23:16:39 GMT
EXPOSE 8080
# Tue, 15 Dec 2020 23:16:40 GMT
WORKDIR /plone/instance
# Tue, 15 Dec 2020 23:16:40 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Tue, 15 Dec 2020 23:16:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 15 Dec 2020 23:16:40 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a294b7a50964d927f56c36d222326194c96b17568893f059084c1fd482dc27`  
		Last Modified: Fri, 11 Dec 2020 15:34:21 GMT  
		Size: 280.8 KB (280809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f0602835631a561ecc8f87fe7ed94eaf444da2bcb33b4d525e8f7c2d62cb8e`  
		Last Modified: Fri, 11 Dec 2020 15:34:19 GMT  
		Size: 11.3 MB (11285239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43527bdab7f3dd363c5165b842042ba104a1aa83b1810f0c1e71e3bd453c0ac8`  
		Last Modified: Fri, 11 Dec 2020 15:34:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fa9d7a2d9fe0122aca9ae94330db35ba5d1e6d727bda05773301d1fa25f17`  
		Last Modified: Tue, 15 Dec 2020 22:39:01 GMT  
		Size: 2.1 MB (2138050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e97bf67477f48b38468e7a986900686f0ec85ed1060ff39c9b0ca314746d8ae`  
		Last Modified: Tue, 15 Dec 2020 23:19:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff739e0c2afaa1721770533852fe15be4f0e7e0f36ffa46d9f6484ebb9492ba`  
		Last Modified: Tue, 15 Dec 2020 23:19:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0406c26ad299e9e70a50e130ec987d58b50bbedd15383cc3fe823d37026851`  
		Last Modified: Tue, 15 Dec 2020 23:20:25 GMT  
		Size: 120.4 MB (120360034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1e89c0f0ac501d60011aa06dbef7fd979805729fd9183899a8893dff1e982`  
		Last Modified: Tue, 15 Dec 2020 23:19:51 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm variant v6

```console
$ docker pull plone@sha256:05531bb2ec2d02003940d3c4d75277008a4dd04f068c5786d09dcf6b7e451111
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135902277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ebea43b6d5d14b6f6fb9e3119426ab3c6e50d29aca1d5536f3f4a3fdda83f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:10:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 06:10:12 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 06:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Thu, 17 Dec 2020 06:31:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 17 Dec 2020 06:31:40 GMT
ENV PYTHON_VERSION=3.8.6
# Thu, 17 Dec 2020 06:40:48 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 17 Dec 2020 06:40:50 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 17 Dec 2020 06:40:52 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Thu, 17 Dec 2020 06:40:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Thu, 17 Dec 2020 06:40:55 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Thu, 17 Dec 2020 06:41:10 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 17 Dec 2020 06:41:12 GMT
CMD ["python3"]
# Thu, 17 Dec 2020 10:15:59 GMT
ENV PIP=20.2.3 ZC_BUILDOUT=2.13.3 SETUPTOOLS=50.3.0 WHEEL=0.35.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.2 PLONE_VERSION_RELEASE=Plone-5.2.2-UnifiedInstaller PLONE_MD5=a603eddfd3abb0528f0861472ebac934
# Thu, 17 Dec 2020 10:16:00 GMT
LABEL plone=5.2.2 os=alpine os.version=3.12 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Thu, 17 Dec 2020 10:16:04 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Thu, 17 Dec 2020 10:16:06 GMT
COPY file:e1c551fc370867c153c440542b0f297049c860021da1d914d102da702cd4376a in /plone/instance/ 
# Thu, 17 Dec 2020 10:32:47 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Thu, 17 Dec 2020 10:32:50 GMT
VOLUME [/data]
# Thu, 17 Dec 2020 10:32:51 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Thu, 17 Dec 2020 10:32:52 GMT
EXPOSE 8080
# Thu, 17 Dec 2020 10:32:53 GMT
WORKDIR /plone/instance
# Thu, 17 Dec 2020 10:32:53 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Thu, 17 Dec 2020 10:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 10:32:55 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58afa002a7f38e3dc8df0d977ab013b084a3589bdc2ca0065d0cea13c04dfc07`  
		Last Modified: Thu, 17 Dec 2020 07:45:09 GMT  
		Size: 281.0 KB (280984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95a5610672b268aa222bee406fbbf2bd21e0e68f5864bd0001cb20718337180`  
		Last Modified: Thu, 17 Dec 2020 07:45:13 GMT  
		Size: 10.9 MB (10914554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1db14576d256964a7cba529462db1d791db04e150dfac137d281c84e1c9abe`  
		Last Modified: Thu, 17 Dec 2020 07:45:08 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bc9691b3dd867bac07b0a007bb0466066715e0230ae349ef3827229adc18f9`  
		Last Modified: Thu, 17 Dec 2020 07:45:10 GMT  
		Size: 2.1 MB (2138372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d734970c640218026ce51f794fe9026b1509bfc9dbe2555f09acc52d41895faf`  
		Last Modified: Thu, 17 Dec 2020 10:33:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce2af9e169d54877399303b796253788697e25175a555dab1306bd09358458a`  
		Last Modified: Thu, 17 Dec 2020 10:33:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650718721cd30fa89b680b9b11f661c7a6314b56c37e132bcc07a1f0a9399015`  
		Last Modified: Thu, 17 Dec 2020 10:34:00 GMT  
		Size: 120.0 MB (119958712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644e39d3e4657d60d3a36560bf1668b43ee174019f3c183c885beffc0e1a6eec`  
		Last Modified: Thu, 17 Dec 2020 10:33:13 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm64 variant v8

```console
$ docker pull plone@sha256:f797b79d01153b2f5f813aab47ff047324ff27e722aad2f4152e70c7d2b956f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136722168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477dbe6daf68941b61f1dc8ef0f22ceeec4064ba6c7182a3c51e632fed5d51d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:50:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 12:23:16 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 13:04:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 11 Dec 2020 13:05:00 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 11 Dec 2020 13:05:08 GMT
ENV PYTHON_VERSION=3.8.6
# Fri, 11 Dec 2020 13:12:21 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 11 Dec 2020 13:12:27 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 15 Dec 2020 22:59:10 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 15 Dec 2020 22:59:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 15 Dec 2020 22:59:13 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 15 Dec 2020 22:59:32 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 15 Dec 2020 22:59:41 GMT
CMD ["python3"]
# Wed, 16 Dec 2020 00:11:13 GMT
ENV PIP=20.2.3 ZC_BUILDOUT=2.13.3 SETUPTOOLS=50.3.0 WHEEL=0.35.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.2 PLONE_VERSION_RELEASE=Plone-5.2.2-UnifiedInstaller PLONE_MD5=a603eddfd3abb0528f0861472ebac934
# Wed, 16 Dec 2020 00:11:15 GMT
LABEL plone=5.2.2 os=alpine os.version=3.12 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 16 Dec 2020 00:11:18 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 16 Dec 2020 00:11:19 GMT
COPY file:e1c551fc370867c153c440542b0f297049c860021da1d914d102da702cd4376a in /plone/instance/ 
# Wed, 16 Dec 2020 00:28:04 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 16 Dec 2020 00:28:12 GMT
VOLUME [/data]
# Wed, 16 Dec 2020 00:28:13 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 16 Dec 2020 00:28:15 GMT
EXPOSE 8080
# Wed, 16 Dec 2020 00:28:16 GMT
WORKDIR /plone/instance
# Wed, 16 Dec 2020 00:28:17 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 16 Dec 2020 00:28:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Dec 2020 00:28:18 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013782172d7687fb9bab7c7236554bfc548042ac8776a51cc3cde1d7d20292cb`  
		Last Modified: Fri, 11 Dec 2020 14:32:00 GMT  
		Size: 281.2 KB (281216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a0881b983c6767039614f638250cb638600976455f086db8e1c86924180a03`  
		Last Modified: Fri, 11 Dec 2020 14:32:02 GMT  
		Size: 11.4 MB (11373513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eff1f7f3f9daa84fe189f2e0f01a34fdb3a9b61b746910e9d015cc385a479f9`  
		Last Modified: Fri, 11 Dec 2020 14:31:59 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10115fa6f61d60dac47906f80df4dcdcb4633fcb188f45c0df156d66771a245a`  
		Last Modified: Tue, 15 Dec 2020 23:10:49 GMT  
		Size: 2.1 MB (2138430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa831772cf8b69a4f71c8ade1cff6451483647663632b6c426314513838e7b0`  
		Last Modified: Wed, 16 Dec 2020 00:31:32 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89587eaba5b65125ef3a907ebd7e166e905b3c4bec64ff4d9f9adfeb036b30`  
		Last Modified: Wed, 16 Dec 2020 00:31:32 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360bca193c8bd0a0be80319325cb8389876ec880db6e2efe2202d6724937dce8`  
		Last Modified: Wed, 16 Dec 2020 00:32:05 GMT  
		Size: 120.2 MB (120216901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77233031fb1fae1dc921351acd732222821140e5a8c0ac5f4f77cc8404b3a73`  
		Last Modified: Wed, 16 Dec 2020 00:31:32 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; 386

```console
$ docker pull plone@sha256:c3550b1107fe61a7cedf1e85e06047cf904d30be2dcf52462d3aa46067c7333e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137227046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c71f61064126dd0bbcee983e11280607c5146de80527b4cf192390d9709a39`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:32 GMT
ADD file:de33fda50a142403e842620d20bc4404e66fc4ace16edc6946c4539e8a797458 in / 
# Thu, 17 Dec 2020 00:38:32 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:08:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 06:08:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 06:25:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Thu, 17 Dec 2020 06:25:24 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 17 Dec 2020 06:25:24 GMT
ENV PYTHON_VERSION=3.8.6
# Thu, 17 Dec 2020 06:32:40 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 17 Dec 2020 06:32:41 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 17 Dec 2020 06:32:41 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Thu, 17 Dec 2020 06:32:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Thu, 17 Dec 2020 06:32:41 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Thu, 17 Dec 2020 06:32:48 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 17 Dec 2020 06:32:48 GMT
CMD ["python3"]
# Thu, 17 Dec 2020 10:41:12 GMT
ENV PIP=20.2.3 ZC_BUILDOUT=2.13.3 SETUPTOOLS=50.3.0 WHEEL=0.35.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.2 PLONE_VERSION_RELEASE=Plone-5.2.2-UnifiedInstaller PLONE_MD5=a603eddfd3abb0528f0861472ebac934
# Thu, 17 Dec 2020 10:41:12 GMT
LABEL plone=5.2.2 os=alpine os.version=3.12 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Thu, 17 Dec 2020 10:41:13 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Thu, 17 Dec 2020 10:41:13 GMT
COPY file:e1c551fc370867c153c440542b0f297049c860021da1d914d102da702cd4376a in /plone/instance/ 
# Thu, 17 Dec 2020 10:57:36 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Thu, 17 Dec 2020 10:57:37 GMT
VOLUME [/data]
# Thu, 17 Dec 2020 10:57:38 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Thu, 17 Dec 2020 10:57:38 GMT
EXPOSE 8080
# Thu, 17 Dec 2020 10:57:38 GMT
WORKDIR /plone/instance
# Thu, 17 Dec 2020 10:57:39 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Thu, 17 Dec 2020 10:57:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 10:57:40 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:455793c72b878001f0905634ed52a2524ba51796e7377bf00683a85123f7dce9`  
		Last Modified: Thu, 17 Dec 2020 00:39:18 GMT  
		Size: 2.8 MB (2794130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8de1c3121b25018c9704e77ea52a95c39db48a341e5bcf9c7bf1f7d28fa019d`  
		Last Modified: Thu, 17 Dec 2020 07:16:58 GMT  
		Size: 281.3 KB (281321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a3dcf765877209d87ec004eaef0819b71e8c5a6ba5796330583abff7f8f218`  
		Last Modified: Thu, 17 Dec 2020 07:17:00 GMT  
		Size: 11.5 MB (11483529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b767678b84bbf4357d455536dfc59521dc0dcc52f31eae1629c113e269eecd38`  
		Last Modified: Thu, 17 Dec 2020 07:16:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e038f334eb03b34bd43db37de66e191142e5200cadd95f288b2712c5f2241fe4`  
		Last Modified: Thu, 17 Dec 2020 07:16:58 GMT  
		Size: 2.1 MB (2138027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c31a5bcd4f10f1b225bb12013ec09fc453bfb5d454eec51d96d4b0149c94e6`  
		Last Modified: Thu, 17 Dec 2020 10:58:40 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f101e9e214a8f8c1de04667c2ec0e42a3de2eaccd933ae3081c6aeb9193a69`  
		Last Modified: Thu, 17 Dec 2020 10:58:39 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0d0c206b3aa66cc60c4df70c1c32bf0de0bcaaee36f5612221b82ecfab08c8`  
		Last Modified: Thu, 17 Dec 2020 10:59:39 GMT  
		Size: 120.5 MB (120524613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0aa1511410308aefb71032727d42a4dc523d47d68cb7b5ac9d1ed6027acd48`  
		Last Modified: Thu, 17 Dec 2020 10:58:40 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; ppc64le

```console
$ docker pull plone@sha256:8937f4573608b746219d15327301befa2b0ea5fae2d83065bce5f73a76f16f50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138086120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1deb1f6eb73eeddc45c47f32290b54b049e609a0662aea2d803a313c20bf875`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 11 Dec 2020 03:30:29 GMT
ADD file:9b4b44ee9eaddedc13f114bb55c9abeabceff6abd47f4a660734e431d22fcdce in / 
# Fri, 11 Dec 2020 03:30:32 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 13:58:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 13:58:52 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 14:50:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 11 Dec 2020 14:50:28 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 11 Dec 2020 14:50:29 GMT
ENV PYTHON_VERSION=3.8.6
# Fri, 11 Dec 2020 14:58:11 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 11 Dec 2020 14:58:19 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 15 Dec 2020 22:40:05 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 15 Dec 2020 22:40:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 15 Dec 2020 22:40:19 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 15 Dec 2020 22:41:07 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 15 Dec 2020 22:41:14 GMT
CMD ["python3"]
# Wed, 16 Dec 2020 00:37:12 GMT
ENV PIP=20.2.3 ZC_BUILDOUT=2.13.3 SETUPTOOLS=50.3.0 WHEEL=0.35.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.2 PLONE_VERSION_RELEASE=Plone-5.2.2-UnifiedInstaller PLONE_MD5=a603eddfd3abb0528f0861472ebac934
# Wed, 16 Dec 2020 00:37:25 GMT
LABEL plone=5.2.2 os=alpine os.version=3.12 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 16 Dec 2020 00:37:56 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 16 Dec 2020 00:37:59 GMT
COPY file:e1c551fc370867c153c440542b0f297049c860021da1d914d102da702cd4376a in /plone/instance/ 
# Wed, 16 Dec 2020 00:57:31 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 16 Dec 2020 00:57:45 GMT
VOLUME [/data]
# Wed, 16 Dec 2020 00:57:49 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 16 Dec 2020 00:57:57 GMT
EXPOSE 8080
# Wed, 16 Dec 2020 00:58:06 GMT
WORKDIR /plone/instance
# Wed, 16 Dec 2020 00:58:14 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 16 Dec 2020 00:58:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Dec 2020 00:58:42 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:ed596bc4dd0a0c7ff1952005f6cae53a061e1c7998282289586bbfc17a2fd6db`  
		Last Modified: Fri, 11 Dec 2020 03:31:06 GMT  
		Size: 2.8 MB (2803424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ec18dc78a565d5f0768349c9ceb1bb4a5e97f1de464739390efa777bc1c3`  
		Last Modified: Fri, 11 Dec 2020 16:04:28 GMT  
		Size: 283.2 KB (283206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc070b7c78ebb64c3ed4975b02f7dcd02f30c51304dc5ef83a9f6528240268`  
		Last Modified: Fri, 11 Dec 2020 16:04:31 GMT  
		Size: 12.0 MB (12032112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62823f8613460cdd3385201be9f8d5e2328a6741574a93a0a356bee453cdf8`  
		Last Modified: Fri, 11 Dec 2020 16:04:28 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d96fcae01700afe86602ab1116b7032102be92af2cd8846340bca96af8508`  
		Last Modified: Tue, 15 Dec 2020 23:01:36 GMT  
		Size: 2.1 MB (2138575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6902d393af22241860a3625dd4fa7d8b72d27d63f8c174fcf0496e702d02ac0a`  
		Last Modified: Wed, 16 Dec 2020 01:06:24 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0926cb28892fa6bfa466a6fffc77dae289d882270f9c6fb84d05efeaf5b642d2`  
		Last Modified: Wed, 16 Dec 2020 01:06:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0727df47e5bea7f790a029c1b130733496699ffb16220a2f646c8b605ce907e`  
		Last Modified: Wed, 16 Dec 2020 01:06:55 GMT  
		Size: 120.8 MB (120823308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b366cef1d22fe205d3280b9191b3c22395329e8627b2243d7bfcef20952878`  
		Last Modified: Wed, 16 Dec 2020 01:06:24 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; s390x

```console
$ docker pull plone@sha256:6384ca6e50f0a1ae18aff714aa1b10518f6ac903578807606d8477d53542eb06
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136340038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3e4984629834bb05e6853ffe6930106bd6774ae340a65a6b9336862b0b8a1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 06:55:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 10:18:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 11 Dec 2020 10:18:49 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 11 Dec 2020 10:18:50 GMT
ENV PYTHON_VERSION=3.8.6
# Fri, 11 Dec 2020 10:24:43 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 11 Dec 2020 10:24:46 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 15 Dec 2020 22:45:23 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 15 Dec 2020 22:45:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 15 Dec 2020 22:45:23 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 15 Dec 2020 22:45:29 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 15 Dec 2020 22:45:30 GMT
CMD ["python3"]
# Tue, 15 Dec 2020 23:24:04 GMT
ENV PIP=20.2.3 ZC_BUILDOUT=2.13.3 SETUPTOOLS=50.3.0 WHEEL=0.35.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.2 PLONE_VERSION_RELEASE=Plone-5.2.2-UnifiedInstaller PLONE_MD5=a603eddfd3abb0528f0861472ebac934
# Tue, 15 Dec 2020 23:24:04 GMT
LABEL plone=5.2.2 os=alpine os.version=3.12 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Tue, 15 Dec 2020 23:24:05 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Tue, 15 Dec 2020 23:24:06 GMT
COPY file:e1c551fc370867c153c440542b0f297049c860021da1d914d102da702cd4376a in /plone/instance/ 
# Tue, 15 Dec 2020 23:31:09 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Tue, 15 Dec 2020 23:31:24 GMT
VOLUME [/data]
# Tue, 15 Dec 2020 23:31:24 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Tue, 15 Dec 2020 23:31:25 GMT
EXPOSE 8080
# Tue, 15 Dec 2020 23:31:25 GMT
WORKDIR /plone/instance
# Tue, 15 Dec 2020 23:31:25 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Tue, 15 Dec 2020 23:31:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 15 Dec 2020 23:31:26 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ae61be5a870639fe07a17526ef280cc170edf9e9daa6c916bd57b397183f01`  
		Last Modified: Fri, 11 Dec 2020 10:57:24 GMT  
		Size: 281.3 KB (281338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b041bcb60246d47257dbbab4739573be68a34ef96dbe0e286f31f1db9e26ba31`  
		Last Modified: Fri, 11 Dec 2020 10:57:25 GMT  
		Size: 11.3 MB (11267243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15275ffc4982fb78b4c8deddbd7aaba762d37f34a48ec9428b4ababa94bc551d`  
		Last Modified: Fri, 11 Dec 2020 10:57:24 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79857d61a61131009cb9bacb8c7a891ca9877fb252ee4bad3f9a08df08530a2`  
		Last Modified: Tue, 15 Dec 2020 22:50:01 GMT  
		Size: 2.1 MB (2138106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca290482da6dd75a654fb7dd8a4d18bb88c5654b351a23a06a556904ed66ded`  
		Last Modified: Tue, 15 Dec 2020 23:33:58 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266e33f0fabe04d4f578af7a9dbcd866b64848d46acc1eb45164d8520d07ffc0`  
		Last Modified: Tue, 15 Dec 2020 23:33:58 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6bf959054ed6580ab835efafc0a819cb89054cdcd692d9877a009b9b3391ec`  
		Last Modified: Tue, 15 Dec 2020 23:34:14 GMT  
		Size: 120.1 MB (120081883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2174c61c89d15de05dd157eb1e78418f9368f58657e070b368213757309f3`  
		Last Modified: Tue, 15 Dec 2020 23:33:58 GMT  
		Size: 2.8 KB (2846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
