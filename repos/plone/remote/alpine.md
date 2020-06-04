## `plone:alpine`

```console
$ docker pull plone@sha256:7f75713f60c7288b6d0618ac2bdccf4c6bf5419d4354aa3ad01d8bdb7f97f926
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
$ docker pull plone@sha256:a1759ac6da3dd5117edc768a46c3f7e83d8da655010b7c1851aa4801b0928782
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150744081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b7a1a385c90671429977595c853c4abcbf87502aa11c163142240f2f5a9f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:48:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2020 19:36:53 GMT
ENV LANG=C.UTF-8
# Wed, 03 Jun 2020 19:36:54 GMT
RUN apk add --no-cache ca-certificates
# Wed, 03 Jun 2020 19:51:35 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 03 Jun 2020 19:51:35 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 03 Jun 2020 20:00:14 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Wed, 03 Jun 2020 20:00:15 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 03 Jun 2020 20:00:15 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Wed, 03 Jun 2020 20:00:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Wed, 03 Jun 2020 20:00:16 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Wed, 03 Jun 2020 20:00:21 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 Jun 2020 20:00:22 GMT
CMD ["python3"]
# Wed, 03 Jun 2020 20:31:14 GMT
ENV PIP=19.3.1 ZC_BUILDOUT=2.13.2 SETUPTOOLS=45.0.0 WHEEL=0.33.6 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.1 PLONE_VERSION_RELEASE=Plone-5.2.1-UnifiedInstaller-r2 PLONE_MD5=42407c0313791d3626dc86e674684efe
# Wed, 03 Jun 2020 20:31:15 GMT
LABEL plone=5.2.1 os=alpine os.version=3.11 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 03 Jun 2020 20:31:15 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 03 Jun 2020 20:31:16 GMT
COPY file:9266bca2e9775c84ef54f877d6d8090bca5c55d7cc6faf7b7226bc188ab30a69 in /plone/instance/ 
# Wed, 03 Jun 2020 20:40:06 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 03 Jun 2020 20:40:07 GMT
VOLUME [/data]
# Wed, 03 Jun 2020 20:40:07 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 03 Jun 2020 20:40:08 GMT
EXPOSE 8080
# Wed, 03 Jun 2020 20:40:08 GMT
WORKDIR /plone/instance
# Wed, 03 Jun 2020 20:40:08 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 03 Jun 2020 20:40:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Jun 2020 20:40:08 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b3adc4ff6ffb76ae233f0a92177205845aaf3e9a39e0f96405dabd1423edc9`  
		Last Modified: Wed, 03 Jun 2020 20:14:46 GMT  
		Size: 280.8 KB (280840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158d3630f7f4b868bf2b25ee253539fd1c4d956da6caa4d49c66ccdc1723aee6`  
		Last Modified: Wed, 03 Jun 2020 20:15:31 GMT  
		Size: 20.7 MB (20668130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656e733c2e63706b6408d5e789912d5ee83ad75e1e82dc32ca77a1b5f7b3eb42`  
		Last Modified: Wed, 03 Jun 2020 20:15:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069d7d2ffc1e156339f57737f61edb8faead64a17297c981d3fabcc9c7f0ba98`  
		Last Modified: Wed, 03 Jun 2020 20:15:28 GMT  
		Size: 1.9 MB (1931845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc08dde55cb3c43b5d07e1546a12d9cb5775c5956264700c8248ddd87face596`  
		Last Modified: Wed, 03 Jun 2020 20:40:31 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f45047250816174c244660d71cb5b937b87d635d0322458cf355315f29dd5c`  
		Last Modified: Wed, 03 Jun 2020 20:40:31 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c0c4109634677ddfd351c35e7c6453a63098576e999cdcffddae7edde2471d`  
		Last Modified: Wed, 03 Jun 2020 20:40:54 GMT  
		Size: 125.1 MB (125060302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906608235a15b5077148dcb2b13cd63e89ff91e9e23c8af12e9bab72d470bdaa`  
		Last Modified: Wed, 03 Jun 2020 20:40:31 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm variant v6

```console
$ docker pull plone@sha256:30e422137b980b4ad0388f9a11218b409be23a777bcc12ef2cbd8c3dfd6da3f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148798185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b319514d412e718a5d47fc314a9aa50e404fc0318bca8fddc7bab4e0be464db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2020 18:59:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2020 18:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 03 Jun 2020 18:59:59 GMT
RUN apk add --no-cache ca-certificates
# Wed, 03 Jun 2020 19:20:17 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 03 Jun 2020 19:20:18 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 03 Jun 2020 19:36:09 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Wed, 03 Jun 2020 19:36:11 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 03 Jun 2020 19:36:12 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Wed, 03 Jun 2020 19:36:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Wed, 03 Jun 2020 19:36:13 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Wed, 03 Jun 2020 19:36:26 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 Jun 2020 19:36:27 GMT
CMD ["python3"]
# Wed, 03 Jun 2020 20:14:49 GMT
ENV PIP=19.3.1 ZC_BUILDOUT=2.13.2 SETUPTOOLS=45.0.0 WHEEL=0.33.6 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.1 PLONE_VERSION_RELEASE=Plone-5.2.1-UnifiedInstaller-r2 PLONE_MD5=42407c0313791d3626dc86e674684efe
# Wed, 03 Jun 2020 20:14:49 GMT
LABEL plone=5.2.1 os=alpine os.version=3.11 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 03 Jun 2020 20:14:51 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 03 Jun 2020 20:14:51 GMT
COPY file:9266bca2e9775c84ef54f877d6d8090bca5c55d7cc6faf7b7226bc188ab30a69 in /plone/instance/ 
# Wed, 03 Jun 2020 20:33:57 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 03 Jun 2020 20:34:03 GMT
VOLUME [/data]
# Wed, 03 Jun 2020 20:34:04 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 03 Jun 2020 20:34:05 GMT
EXPOSE 8080
# Wed, 03 Jun 2020 20:34:05 GMT
WORKDIR /plone/instance
# Wed, 03 Jun 2020 20:34:06 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 03 Jun 2020 20:34:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Jun 2020 20:34:07 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba84132d8cf30d261b7b1e4e503e67af8ea432e7f530a830161cc1b1bd53e82`  
		Last Modified: Wed, 03 Jun 2020 19:55:42 GMT  
		Size: 281.0 KB (281040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b48db2076031d02a2f20c53bde81748b024b59a8f1f674ef1c03513a4eb0e0`  
		Last Modified: Wed, 03 Jun 2020 19:56:32 GMT  
		Size: 19.2 MB (19198124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c60c485eb29b1f0779f2afed0218c89fab4965fa17233e6db168bfdea71c056`  
		Last Modified: Wed, 03 Jun 2020 19:56:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91216ddcdfa0559f3f992bd378ee278a17d3a8af05e9cc7610b0b668f5c4c435`  
		Last Modified: Wed, 03 Jun 2020 19:56:26 GMT  
		Size: 1.9 MB (1932089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2be147a3119a6b5bf3960f612deb504b2374932f0c9eac394d9cfa2acc1838`  
		Last Modified: Wed, 03 Jun 2020 20:34:20 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d68d354122a83e4f1c649a6dfa2f6b7d860f79d6c13759f6e4b00d4d78e050`  
		Last Modified: Wed, 03 Jun 2020 20:34:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f432ea1d74bc47ea1b45a2b269129078ca16cfd55bee0c3bd8e5d43a0eb1fc2d`  
		Last Modified: Wed, 03 Jun 2020 20:35:07 GMT  
		Size: 124.8 MB (124778164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f0786d06f845ed783d5cc5c36c4788fe6c40e9e27873c656894d813a5751a`  
		Last Modified: Wed, 03 Jun 2020 20:34:20 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm64 variant v8

```console
$ docker pull plone@sha256:04238a3f4f43e77921c3423f7157754215bc61b52e5253fdab5a5ff4194f6019
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150320058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21ad7d54c80f970fbf8323a7175b2aade0206f4d47147a6059580ba102d783f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:35:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2020 18:57:57 GMT
ENV LANG=C.UTF-8
# Wed, 03 Jun 2020 18:58:00 GMT
RUN apk add --no-cache ca-certificates
# Wed, 03 Jun 2020 19:14:44 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 03 Jun 2020 19:14:45 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 03 Jun 2020 19:28:47 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Wed, 03 Jun 2020 19:28:51 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 03 Jun 2020 19:28:52 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Wed, 03 Jun 2020 19:28:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Wed, 03 Jun 2020 19:28:53 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Wed, 03 Jun 2020 19:29:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 Jun 2020 19:29:04 GMT
CMD ["python3"]
# Wed, 03 Jun 2020 20:03:56 GMT
ENV PIP=19.3.1 ZC_BUILDOUT=2.13.2 SETUPTOOLS=45.0.0 WHEEL=0.33.6 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.1 PLONE_VERSION_RELEASE=Plone-5.2.1-UnifiedInstaller-r2 PLONE_MD5=42407c0313791d3626dc86e674684efe
# Wed, 03 Jun 2020 20:03:57 GMT
LABEL plone=5.2.1 os=alpine os.version=3.11 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 03 Jun 2020 20:03:58 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 03 Jun 2020 20:03:59 GMT
COPY file:9266bca2e9775c84ef54f877d6d8090bca5c55d7cc6faf7b7226bc188ab30a69 in /plone/instance/ 
# Wed, 03 Jun 2020 20:22:09 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 03 Jun 2020 20:22:14 GMT
VOLUME [/data]
# Wed, 03 Jun 2020 20:22:14 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 03 Jun 2020 20:22:15 GMT
EXPOSE 8080
# Wed, 03 Jun 2020 20:22:16 GMT
WORKDIR /plone/instance
# Wed, 03 Jun 2020 20:22:16 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 03 Jun 2020 20:22:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Jun 2020 20:22:17 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d489d24c26399308b276dfa175c049e531d2686fb99e250ad3ede210fd01e9e`  
		Last Modified: Wed, 03 Jun 2020 19:46:54 GMT  
		Size: 281.3 KB (281267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7456013ab581507a5ee7cfd546ae1c0f55ea6bd8cc9111166f0ab67914310a2`  
		Last Modified: Wed, 03 Jun 2020 19:47:46 GMT  
		Size: 20.6 MB (20567069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7af659da21e90827a775093fe36b17db0e84e272d2d3b0a3af0b36d948c4b6`  
		Last Modified: Wed, 03 Jun 2020 19:47:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5846b63f09167daa484912c36e319edd35e5ff3ecc492249cd4f9e18d11e6e4a`  
		Last Modified: Wed, 03 Jun 2020 19:47:40 GMT  
		Size: 1.9 MB (1932063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed2daffe731b676938dcbe190a049251a824276ad562f08f49852d03ea8e0c`  
		Last Modified: Wed, 03 Jun 2020 20:22:52 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ce0d96188c3281813cf4e022f52d8617969568d783044ac0658811fe52c5f8`  
		Last Modified: Wed, 03 Jun 2020 20:22:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f461b3ea68e07d7a475d07a1f9a0595d0aed75a9b20b06f46ad2a1018cfc7fc`  
		Last Modified: Wed, 03 Jun 2020 20:23:30 GMT  
		Size: 124.8 MB (124826213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a10d5e9ff76209b169f5f9348fd4094874e9bfbbe148ba8df8e11e3775fbf57`  
		Last Modified: Wed, 03 Jun 2020 20:22:52 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; 386

```console
$ docker pull plone@sha256:b0952c68d8ed16e73d0384002377f7db910517c74ff393ad71d3b7a87a962ce3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149936038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411dd60f3b31b5f1d02af436f2330ed09bca6cf7f8f2cba528b27575897ded2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2020 18:45:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2020 18:45:48 GMT
ENV LANG=C.UTF-8
# Wed, 03 Jun 2020 18:45:49 GMT
RUN apk add --no-cache ca-certificates
# Wed, 03 Jun 2020 19:02:15 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 03 Jun 2020 19:02:16 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 03 Jun 2020 19:11:40 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Wed, 03 Jun 2020 19:11:41 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 03 Jun 2020 19:11:41 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Wed, 03 Jun 2020 19:11:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Wed, 03 Jun 2020 19:11:41 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Wed, 03 Jun 2020 19:11:48 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 Jun 2020 19:11:48 GMT
CMD ["python3"]
# Wed, 03 Jun 2020 19:49:09 GMT
ENV PIP=19.3.1 ZC_BUILDOUT=2.13.2 SETUPTOOLS=45.0.0 WHEEL=0.33.6 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.1 PLONE_VERSION_RELEASE=Plone-5.2.1-UnifiedInstaller-r2 PLONE_MD5=42407c0313791d3626dc86e674684efe
# Wed, 03 Jun 2020 19:49:09 GMT
LABEL plone=5.2.1 os=alpine os.version=3.11 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 03 Jun 2020 19:49:11 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 03 Jun 2020 19:49:11 GMT
COPY file:9266bca2e9775c84ef54f877d6d8090bca5c55d7cc6faf7b7226bc188ab30a69 in /plone/instance/ 
# Wed, 03 Jun 2020 20:02:21 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 03 Jun 2020 20:02:23 GMT
VOLUME [/data]
# Wed, 03 Jun 2020 20:02:23 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 03 Jun 2020 20:02:24 GMT
EXPOSE 8080
# Wed, 03 Jun 2020 20:02:24 GMT
WORKDIR /plone/instance
# Wed, 03 Jun 2020 20:02:25 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 03 Jun 2020 20:02:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Jun 2020 20:02:25 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded523869d7b2121c2a5838365e9f75504b850ecae6661c940242d3456bd53d7`  
		Last Modified: Wed, 03 Jun 2020 19:28:31 GMT  
		Size: 281.4 KB (281373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232066e005399326494e8e9c39ab14c83a4d89f9b44406145ac8e9bd6fc84224`  
		Last Modified: Wed, 03 Jun 2020 19:29:25 GMT  
		Size: 19.9 MB (19862047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f21ab5913bf51be9cc838c07b52725fd721304e4a78524c5ac91892385487`  
		Last Modified: Wed, 03 Jun 2020 19:29:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afde129237160f73b2b11696ea5eed2f6f5285766b9747de5ebcdccc156332b0`  
		Last Modified: Wed, 03 Jun 2020 19:29:10 GMT  
		Size: 1.9 MB (1931749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a43a2279c3802c4110bd925fa017e9a365514d6b0031d3ffd4f15430e3787f3`  
		Last Modified: Wed, 03 Jun 2020 20:02:52 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39df8240f53bd3dbf405cd37fe09aabbce3030fbd2aa14ffe0dce50ae48964e`  
		Last Modified: Wed, 03 Jun 2020 20:02:51 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f5abda154d848d944bcc715f5041c3d5f12c318574eb17cb47988af4df709`  
		Last Modified: Wed, 03 Jun 2020 20:03:42 GMT  
		Size: 125.1 MB (125063149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a76190bf3a2d889125eb2027978b2842a77544a1932cccc2a8075840171dc1`  
		Last Modified: Wed, 03 Jun 2020 20:02:52 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; ppc64le

```console
$ docker pull plone@sha256:b6db91be2f9da284f0439af7ebf2c3e0ec9ef03c40080a61391e9872f8cd1cae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152080232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2370e99009fb1cad64f533bd25fde7c359791c4a9aaf930f34d8d2a87da3c07b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2020 19:35:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2020 19:35:58 GMT
ENV LANG=C.UTF-8
# Wed, 03 Jun 2020 19:36:09 GMT
RUN apk add --no-cache ca-certificates
# Wed, 03 Jun 2020 19:54:46 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 03 Jun 2020 19:54:48 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 03 Jun 2020 20:06:42 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Wed, 03 Jun 2020 20:06:54 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 03 Jun 2020 20:06:56 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Wed, 03 Jun 2020 20:06:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Wed, 03 Jun 2020 20:07:04 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Wed, 03 Jun 2020 20:07:23 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 Jun 2020 20:07:26 GMT
CMD ["python3"]
# Wed, 03 Jun 2020 20:48:07 GMT
ENV PIP=19.3.1 ZC_BUILDOUT=2.13.2 SETUPTOOLS=45.0.0 WHEEL=0.33.6 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.1 PLONE_VERSION_RELEASE=Plone-5.2.1-UnifiedInstaller-r2 PLONE_MD5=42407c0313791d3626dc86e674684efe
# Wed, 03 Jun 2020 20:48:11 GMT
LABEL plone=5.2.1 os=alpine os.version=3.11 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 03 Jun 2020 20:48:25 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 03 Jun 2020 20:48:27 GMT
COPY file:9266bca2e9775c84ef54f877d6d8090bca5c55d7cc6faf7b7226bc188ab30a69 in /plone/instance/ 
# Wed, 03 Jun 2020 21:06:08 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 03 Jun 2020 21:06:21 GMT
VOLUME [/data]
# Wed, 03 Jun 2020 21:06:23 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 03 Jun 2020 21:06:25 GMT
EXPOSE 8080
# Wed, 03 Jun 2020 21:06:28 GMT
WORKDIR /plone/instance
# Wed, 03 Jun 2020 21:06:31 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 03 Jun 2020 21:06:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Jun 2020 21:06:38 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9759563702d3bc987f9dad6559da6de6fa68093dc6b51fb097c1c4abc1876`  
		Last Modified: Wed, 03 Jun 2020 20:26:29 GMT  
		Size: 285.0 KB (285014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd87b5f0f6427363db51cf43e2f5430a37ed8ea5aa7e9ec4ce7e44f792bb26`  
		Last Modified: Wed, 03 Jun 2020 20:27:32 GMT  
		Size: 21.7 MB (21713979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b447b0e19f608a18511fb6a37128291ba6875b98619bd866693cae515d02a3a`  
		Last Modified: Wed, 03 Jun 2020 20:27:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8e8908743d4fce3d36bd848b2890bbd7f65d725af7c8db922e34a62fffd278`  
		Last Modified: Wed, 03 Jun 2020 20:27:27 GMT  
		Size: 1.9 MB (1932052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488e92e8a77f721a64aa761852e1954f3487830fb59ed1f0aad82394dcf1cae`  
		Last Modified: Wed, 03 Jun 2020 21:07:12 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9275f0cd3deb9518cf88a92e7cee7e8828ba73f9e86ba877e0e82294f43bbb85`  
		Last Modified: Wed, 03 Jun 2020 21:07:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0854060e04641d983949cfee9d19e284321cfc149472f9cf9fb8bf3ac18f633`  
		Last Modified: Wed, 03 Jun 2020 21:07:40 GMT  
		Size: 125.3 MB (125338500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a32aa6efec13adf7cb813ccc27397b870f9e8ce6ead530e2cf9a880ffb3d8e`  
		Last Modified: Wed, 03 Jun 2020 21:07:11 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; s390x

```console
$ docker pull plone@sha256:36bbec3d11910a472a91ec069105fb1014fd6dc65c48bd662ff80877b17d6977
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150602272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45ad4173c0cd18aeaf612a703b5c0cf27fb0ffd74237ced0cb14b3f23e3659b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2020 19:13:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2020 19:13:11 GMT
ENV LANG=C.UTF-8
# Wed, 03 Jun 2020 19:13:14 GMT
RUN apk add --no-cache ca-certificates
# Wed, 03 Jun 2020 19:26:12 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 03 Jun 2020 19:26:12 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 03 Jun 2020 19:33:02 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Wed, 03 Jun 2020 19:33:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 03 Jun 2020 19:33:06 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Wed, 03 Jun 2020 19:33:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Wed, 03 Jun 2020 19:33:07 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Wed, 03 Jun 2020 19:33:13 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 Jun 2020 19:33:13 GMT
CMD ["python3"]
# Wed, 03 Jun 2020 23:11:01 GMT
ENV PIP=19.3.1 ZC_BUILDOUT=2.13.2 SETUPTOOLS=45.0.0 WHEEL=0.33.6 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.1 PLONE_VERSION_RELEASE=Plone-5.2.1-UnifiedInstaller-r2 PLONE_MD5=42407c0313791d3626dc86e674684efe
# Wed, 03 Jun 2020 23:11:01 GMT
LABEL plone=5.2.1 os=alpine os.version=3.11 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Wed, 03 Jun 2020 23:11:02 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 03 Jun 2020 23:11:02 GMT
COPY file:9266bca2e9775c84ef54f877d6d8090bca5c55d7cc6faf7b7226bc188ab30a69 in /plone/instance/ 
# Wed, 03 Jun 2020 23:18:04 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Wed, 03 Jun 2020 23:18:28 GMT
VOLUME [/data]
# Wed, 03 Jun 2020 23:18:29 GMT
COPY multi:96b4b1619dec8ba8c0507bd3de7fe85d75d30049c6ebd1a2599a7df4353563e5 in / 
# Wed, 03 Jun 2020 23:18:30 GMT
EXPOSE 8080
# Wed, 03 Jun 2020 23:18:30 GMT
WORKDIR /plone/instance
# Wed, 03 Jun 2020 23:18:31 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 03 Jun 2020 23:18:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Jun 2020 23:18:32 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b76e1d722a55ff4f330c758d9814944d8ab0c8761b42febad3c13edcbc7d4f`  
		Last Modified: Wed, 03 Jun 2020 22:40:13 GMT  
		Size: 281.4 KB (281387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c95162056f82d76161ce423bb0cfe8d358456ff9d3ca010abcece1d6ca121f`  
		Last Modified: Wed, 03 Jun 2020 22:40:46 GMT  
		Size: 21.0 MB (20975819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e0761a409a0d5bdad907cc10516a1c81a8dd9da6fb344455f15601791be0cf`  
		Last Modified: Wed, 03 Jun 2020 22:40:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ff0a74e1358d1e08f58f8568c4d045738fc761f9c19b0eeb09e5fc8f9b8648`  
		Last Modified: Wed, 03 Jun 2020 22:40:49 GMT  
		Size: 1.9 MB (1932074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b3c389cbd6efcb2e9c8b4601fbb9f4283d706852a5460b561e8be6328f0c8a`  
		Last Modified: Wed, 03 Jun 2020 23:18:54 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94b74ebd189c956859752316d5e7a10e3282c51870b4a7d377e99a33ae8cf09`  
		Last Modified: Wed, 03 Jun 2020 23:18:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7898dc994ac49903da66f2ad75fef83828275471973c9865956b7d599de94c`  
		Last Modified: Wed, 03 Jun 2020 23:19:16 GMT  
		Size: 124.8 MB (124841326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10139547e077c63c869874d4341c0016e7b76187b8b21652c8f81e09c207076a`  
		Last Modified: Wed, 03 Jun 2020 23:18:58 GMT  
		Size: 2.8 KB (2846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
