## `plone:alpine`

```console
$ docker pull plone@sha256:b1a13f02fd9e06766147f7736a3d67b2113a2079a3d88153077353caec98cd60
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
$ docker pull plone@sha256:92b3874dc38280cb26a750cbbc0fe4f9bf4c22383bce38bcfc2fc8ba904721bb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160662997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fbf26c91e3cda1e9ade91125e8bb49427422e7d2ea7feb2ea8c6fc83350b16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:28:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2019 19:53:36 GMT
ENV LANG=C.UTF-8
# Mon, 21 Oct 2019 19:53:37 GMT
RUN apk add --no-cache ca-certificates
# Mon, 21 Oct 2019 20:05:00 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 20 Dec 2019 23:19:07 GMT
ENV PYTHON_VERSION=3.7.6
# Sat, 21 Dec 2019 08:29:53 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Sat, 21 Dec 2019 08:29:54 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 21 Dec 2019 08:29:54 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 08:29:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 08:29:54 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 08:29:59 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 08:29:59 GMT
CMD ["python3"]
# Sat, 21 Dec 2019 08:43:09 GMT
ENV PIP=19.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=41.0.0 WHEEL=0.33.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2 PLONE_VERSION_RELEASE=5.2.0 PLONE_MD5=211ff749422611db2e448dea639e1fba
# Sat, 21 Dec 2019 08:43:10 GMT
LABEL plone=5.2 os=alpine os.version=3.10 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Sat, 21 Dec 2019 08:43:10 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sat, 21 Dec 2019 08:43:10 GMT
COPY file:443d87cbc872ff84a1cc60cabe0940e8126ef435a982c2b29ffcc415ca0d5fd0 in /plone/instance/ 
# Sat, 21 Dec 2019 08:50:39 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/base_skeleton/* /plone/instance/ && cp -v ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Sat, 21 Dec 2019 08:50:40 GMT
VOLUME [/data]
# Sat, 21 Dec 2019 08:50:40 GMT
COPY multi:c1f88121bdba3f4019314daa8a4906c592b99b3ebbde00413dc4680482b6d329 in / 
# Sat, 21 Dec 2019 08:50:41 GMT
EXPOSE 8080
# Sat, 21 Dec 2019 08:50:41 GMT
WORKDIR /plone/instance
# Sat, 21 Dec 2019 08:50:41 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 21 Dec 2019 08:50:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 21 Dec 2019 08:50:41 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910c49c00810270202e88365d51e9aed81dc7afd1be0bdb6b1e6c3d08e85b225`  
		Last Modified: Mon, 21 Oct 2019 20:36:24 GMT  
		Size: 301.7 KB (301712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38896355043699e63503985c3f848f33c2578a14418645f983827ae7496cd08c`  
		Last Modified: Sat, 21 Dec 2019 08:38:52 GMT  
		Size: 28.9 MB (28900901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371e684087e4d9fe417ac5fada74b9e68d4ce9789200dd53b93af5ef195a77`  
		Last Modified: Sat, 21 Dec 2019 08:38:47 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118e7b78645bfa13a74d142f72dae8116895389c371d1ec8e0e000f474254e8b`  
		Last Modified: Sat, 21 Dec 2019 08:38:47 GMT  
		Size: 1.9 MB (1870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56b4795269b3e95baaa305d2e3e4b232ae060ac96ec03d8a63ed987ebee0a20`  
		Last Modified: Sat, 21 Dec 2019 09:24:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01705fcdc6b61c1f193d51b0a114c776d7783e8395d3dbff01c637f95557d189`  
		Last Modified: Sat, 21 Dec 2019 09:24:19 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651d38882629215b5645c5ec39b3ea467c5c01694308bad137bf78260087442f`  
		Last Modified: Sat, 21 Dec 2019 09:24:51 GMT  
		Size: 126.8 MB (126797794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5724fd43d5bd1259e2c944ab0805301c8b91c61aca00303af0f34cb3594fd6b3`  
		Last Modified: Sat, 21 Dec 2019 09:24:19 GMT  
		Size: 2.6 KB (2626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm variant v6

```console
$ docker pull plone@sha256:96a1f323737b76c23ca7c1acced672bdf7694f8c8b4a3a3771e613108933de18
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160140857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a576f36b7bfd7d72af268668e454c63d50e7117cb6dd0bf0dd934b2131c72a2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 23:15:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2019 23:15:23 GMT
ENV LANG=C.UTF-8
# Thu, 26 Dec 2019 23:15:25 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 Dec 2019 23:34:38 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 26 Dec 2019 23:34:39 GMT
ENV PYTHON_VERSION=3.7.6
# Thu, 26 Dec 2019 23:50:57 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 26 Dec 2019 23:51:03 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 26 Dec 2019 23:51:06 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 23:51:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 23:51:10 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 23:51:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 23:51:30 GMT
CMD ["python3"]
# Fri, 27 Dec 2019 01:56:46 GMT
ENV PIP=19.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=41.0.0 WHEEL=0.33.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2 PLONE_VERSION_RELEASE=5.2.0 PLONE_MD5=211ff749422611db2e448dea639e1fba
# Fri, 27 Dec 2019 01:56:47 GMT
LABEL plone=5.2 os=alpine os.version=3.10 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Fri, 27 Dec 2019 01:56:50 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 27 Dec 2019 01:56:51 GMT
COPY file:443d87cbc872ff84a1cc60cabe0940e8126ef435a982c2b29ffcc415ca0d5fd0 in /plone/instance/ 
# Fri, 27 Dec 2019 02:14:27 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/base_skeleton/* /plone/instance/ && cp -v ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Fri, 27 Dec 2019 02:14:38 GMT
VOLUME [/data]
# Fri, 27 Dec 2019 02:14:38 GMT
COPY multi:c1f88121bdba3f4019314daa8a4906c592b99b3ebbde00413dc4680482b6d329 in / 
# Fri, 27 Dec 2019 02:14:39 GMT
EXPOSE 8080
# Fri, 27 Dec 2019 02:14:40 GMT
WORKDIR /plone/instance
# Fri, 27 Dec 2019 02:14:41 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 27 Dec 2019 02:14:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 02:14:42 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6c16b3eec9526bd852c13a7869f2bddf5cab8e7762dac1f13fcb5c20f7d32a`  
		Last Modified: Fri, 27 Dec 2019 00:56:38 GMT  
		Size: 301.6 KB (301625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf91e59aa138424f559af56d16406029f93351dfa8e31dec01ed27cd6ccafa3`  
		Last Modified: Fri, 27 Dec 2019 00:57:35 GMT  
		Size: 28.1 MB (28067652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d18fb9c2c37038c3249bb4b8087818084fba3f64bf76d6292c7772c5654fad`  
		Last Modified: Fri, 27 Dec 2019 00:57:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9dcea61c436c55e52e6eb63bab0ede7c8c5e1e5608d2b5c07bebce3eeaa616`  
		Last Modified: Fri, 27 Dec 2019 00:57:25 GMT  
		Size: 1.9 MB (1870479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525d19db73ad646a44b214fd1f45885f51e2c4452b8c2c13f1f6182232e04623`  
		Last Modified: Fri, 27 Dec 2019 02:54:03 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4559f73df6806000bb09bf2fb7c8ad1ee66785a6245b91056b2f6894d8dfe`  
		Last Modified: Fri, 27 Dec 2019 02:54:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566789f1056ac527974216dc5297d3f6fc752fbe8c49d081f0d1bc2a757e5f1e`  
		Last Modified: Fri, 27 Dec 2019 02:54:54 GMT  
		Size: 127.3 MB (127283818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed883831ada9d1492c52664d47b5d1b3f820ff40ce8717b6991c75a0ea441bca`  
		Last Modified: Fri, 27 Dec 2019 02:54:03 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm64 variant v8

```console
$ docker pull plone@sha256:85ee41c2a688a3dbe71a1dfce4ce2db3a51e7c9f5ba403967a139e328a5b5a1d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159805140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a7fa5adc8c5c417a982765fd8921bd3a6a8dc82d9719e596d51ba6dbcc47ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 19:46:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2019 22:35:43 GMT
ENV LANG=C.UTF-8
# Mon, 21 Oct 2019 22:35:45 GMT
RUN apk add --no-cache ca-certificates
# Mon, 21 Oct 2019 22:44:09 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 20 Dec 2019 22:22:54 GMT
ENV PYTHON_VERSION=3.7.6
# Fri, 20 Dec 2019 22:36:54 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 20 Dec 2019 22:36:57 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 20 Dec 2019 22:36:58 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 20 Dec 2019 22:36:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 20 Dec 2019 22:36:59 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 20 Dec 2019 22:37:09 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 20 Dec 2019 22:37:10 GMT
CMD ["python3"]
# Sat, 21 Dec 2019 03:36:48 GMT
ENV PIP=19.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=41.0.0 WHEEL=0.33.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2 PLONE_VERSION_RELEASE=5.2.0 PLONE_MD5=211ff749422611db2e448dea639e1fba
# Sat, 21 Dec 2019 03:36:49 GMT
LABEL plone=5.2 os=alpine os.version=3.10 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Sat, 21 Dec 2019 03:36:50 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sat, 21 Dec 2019 03:36:51 GMT
COPY file:443d87cbc872ff84a1cc60cabe0940e8126ef435a982c2b29ffcc415ca0d5fd0 in /plone/instance/ 
# Sat, 21 Dec 2019 03:52:33 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/base_skeleton/* /plone/instance/ && cp -v ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Sat, 21 Dec 2019 03:52:47 GMT
VOLUME [/data]
# Sat, 21 Dec 2019 03:52:48 GMT
COPY multi:c1f88121bdba3f4019314daa8a4906c592b99b3ebbde00413dc4680482b6d329 in / 
# Sat, 21 Dec 2019 03:52:49 GMT
EXPOSE 8080
# Sat, 21 Dec 2019 03:52:50 GMT
WORKDIR /plone/instance
# Sat, 21 Dec 2019 03:52:51 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 21 Dec 2019 03:52:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 21 Dec 2019 03:52:52 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b9474c28b5b5c139acda2e0c522c02719548cd39edd5d84eda8a8a2994f34`  
		Last Modified: Mon, 21 Oct 2019 23:20:14 GMT  
		Size: 302.3 KB (302343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24596adf7e9aaf06d4ec9e03fa1c30e6aa0d66acde938c2398d364a025f4998b`  
		Last Modified: Sat, 21 Dec 2019 01:42:57 GMT  
		Size: 28.3 MB (28307041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b6e59854cdff539fd2b2c624e827c8ba976013fbf178912739dc1c8cf463e2`  
		Last Modified: Sat, 21 Dec 2019 01:42:48 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cb540bcb6229ac0d1873f082731868ae3392a06796ff646c8c5cb42459d610`  
		Last Modified: Sat, 21 Dec 2019 01:42:48 GMT  
		Size: 1.9 MB (1870463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe7f21dcf0177d70728cbbd9900450489d1d3d0538838e188cfac5591a6bcf`  
		Last Modified: Sat, 21 Dec 2019 05:16:11 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db2c143106a050c86f4992e9fe94bdafcd0f8099da1dd6ccdb36e80db63ec4f`  
		Last Modified: Sat, 21 Dec 2019 05:16:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78de06bf58f4fbd39e5cca169743e5045984fcc9244be6af95697b5dbfb24b0`  
		Last Modified: Sat, 21 Dec 2019 05:16:53 GMT  
		Size: 126.6 MB (126602230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589be6e7d5c2e177f23d74f07ffd63dbcffdc9d228844b540d70b74e4a795501`  
		Last Modified: Sat, 21 Dec 2019 05:16:11 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; 386

```console
$ docker pull plone@sha256:321383f670c66292b4982ed294c984244018c64f97710deba5d426da294dcff1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161073254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282c9d976f54d06fa939e4c541ab3a90443714896723644fbc7f1b0d8ba4ca9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Fri, 27 Dec 2019 00:13:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Dec 2019 00:13:09 GMT
ENV LANG=C.UTF-8
# Fri, 27 Dec 2019 00:13:11 GMT
RUN apk add --no-cache ca-certificates
# Fri, 27 Dec 2019 00:28:43 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 27 Dec 2019 00:28:44 GMT
ENV PYTHON_VERSION=3.7.6
# Fri, 27 Dec 2019 00:38:12 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 27 Dec 2019 00:38:13 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 27 Dec 2019 00:38:13 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 27 Dec 2019 00:38:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 27 Dec 2019 00:38:13 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 27 Dec 2019 00:38:19 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 27 Dec 2019 00:38:19 GMT
CMD ["python3"]
# Fri, 27 Dec 2019 02:17:42 GMT
ENV PIP=19.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=41.0.0 WHEEL=0.33.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2 PLONE_VERSION_RELEASE=5.2.0 PLONE_MD5=211ff749422611db2e448dea639e1fba
# Fri, 27 Dec 2019 02:17:43 GMT
LABEL plone=5.2 os=alpine os.version=3.10 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Fri, 27 Dec 2019 02:17:43 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 27 Dec 2019 02:17:44 GMT
COPY file:443d87cbc872ff84a1cc60cabe0940e8126ef435a982c2b29ffcc415ca0d5fd0 in /plone/instance/ 
# Fri, 27 Dec 2019 02:27:23 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/base_skeleton/* /plone/instance/ && cp -v ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Fri, 27 Dec 2019 02:27:24 GMT
VOLUME [/data]
# Fri, 27 Dec 2019 02:27:24 GMT
COPY multi:c1f88121bdba3f4019314daa8a4906c592b99b3ebbde00413dc4680482b6d329 in / 
# Fri, 27 Dec 2019 02:27:24 GMT
EXPOSE 8080
# Fri, 27 Dec 2019 02:27:24 GMT
WORKDIR /plone/instance
# Fri, 27 Dec 2019 02:27:25 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 27 Dec 2019 02:27:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 02:27:25 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de240d6a1653e8f4fee6d2e829ab2076b8e8e04e235bad27b7f4c2959c5959a`  
		Last Modified: Fri, 27 Dec 2019 01:25:06 GMT  
		Size: 301.9 KB (301907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9a904680d254795292b9927eb314cc37936d27d510fb9442c6525fbd3d025f`  
		Last Modified: Fri, 27 Dec 2019 01:25:42 GMT  
		Size: 28.8 MB (28804138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b11b2cdfbc650af9dd82211a3de15734fcb953fd652c34cbe3c1faa0c80b44a`  
		Last Modified: Fri, 27 Dec 2019 01:25:36 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe642c190b94b51fa8303869f726f270e637950f7f2ee189ebd400f2409d563`  
		Last Modified: Fri, 27 Dec 2019 01:25:37 GMT  
		Size: 1.9 MB (1870197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f280052913e4bd68ca207e38b77e0de759136882c2f7a5f86ad7259b5bb514`  
		Last Modified: Fri, 27 Dec 2019 02:49:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcef3b0ef7ddea3e7315ec6144ddaab8b41510b0ad078afacb15775804c22f4`  
		Last Modified: Fri, 27 Dec 2019 02:49:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa635b79f5b258210bb577686d26f4979cf0dcaa0c53a419511534d33cb7c29b`  
		Last Modified: Fri, 27 Dec 2019 02:49:59 GMT  
		Size: 127.3 MB (127286671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f2978d342b8c1078634bd78e3aba68cbf91bd7dcbc07979fe294805dc9769c`  
		Last Modified: Fri, 27 Dec 2019 02:49:25 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; ppc64le

```console
$ docker pull plone@sha256:c932447e4bc48069d49225d0b43e2594d931fa147f86d0ded6ab245abef847ec
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba63872d1cadd68ce85aae5a8eb1e781b36c5a1780bf118ae10fa4d3a68c667`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Mon, 21 Oct 2019 17:52:55 GMT
ADD file:11a2dd0058b1642e9ee52239d03223819a53ca346fd42826eead7729c50e1257 in / 
# Mon, 21 Oct 2019 17:53:00 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 21:51:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2019 21:51:50 GMT
ENV LANG=C.UTF-8
# Mon, 21 Oct 2019 21:51:57 GMT
RUN apk add --no-cache ca-certificates
# Mon, 21 Oct 2019 22:01:26 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 21 Dec 2019 00:28:33 GMT
ENV PYTHON_VERSION=3.7.6
# Sat, 21 Dec 2019 00:40:30 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Sat, 21 Dec 2019 00:40:36 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 21 Dec 2019 00:40:38 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 00:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 00:40:50 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 00:41:04 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 00:41:06 GMT
CMD ["python3"]
# Sat, 21 Dec 2019 05:48:59 GMT
ENV PIP=19.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=41.0.0 WHEEL=0.33.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2 PLONE_VERSION_RELEASE=5.2.0 PLONE_MD5=211ff749422611db2e448dea639e1fba
# Sat, 21 Dec 2019 05:49:02 GMT
LABEL plone=5.2 os=alpine os.version=3.10 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Sat, 21 Dec 2019 05:49:11 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sat, 21 Dec 2019 05:49:12 GMT
COPY file:443d87cbc872ff84a1cc60cabe0940e8126ef435a982c2b29ffcc415ca0d5fd0 in /plone/instance/ 
# Sat, 21 Dec 2019 06:04:47 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/base_skeleton/* /plone/instance/ && cp -v ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Sat, 21 Dec 2019 06:04:53 GMT
VOLUME [/data]
# Sat, 21 Dec 2019 06:04:54 GMT
COPY multi:c1f88121bdba3f4019314daa8a4906c592b99b3ebbde00413dc4680482b6d329 in / 
# Sat, 21 Dec 2019 06:04:58 GMT
EXPOSE 8080
# Sat, 21 Dec 2019 06:05:03 GMT
WORKDIR /plone/instance
# Sat, 21 Dec 2019 06:05:06 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 21 Dec 2019 06:05:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 21 Dec 2019 06:05:14 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:cd18d16ea896a0f0eb99be52a9722ffae9a5ac35cf28cb8b96f589352f8e71d6`  
		Last Modified: Mon, 21 Oct 2019 17:53:53 GMT  
		Size: 2.8 MB (2808504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dc13f6a3e4e29bf119cf7d30cb66e8f761f84d276827850b19128e670ea34d`  
		Last Modified: Mon, 21 Oct 2019 22:36:28 GMT  
		Size: 304.5 KB (304451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9317e5bbc4d97941fb141c1db1b7a027a96472213c2c0e6034c7c784f1c2b65`  
		Last Modified: Sat, 21 Dec 2019 04:01:20 GMT  
		Size: 29.9 MB (29935663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11e7de7042b5ecc0f97445c79d3ab9ff96e931ac94d4bb3f228cc3a3dd7da50`  
		Last Modified: Sat, 21 Dec 2019 04:01:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b750d298c91da77cc48d6a05ff0b08bb42d72e80cb9ad5e7083cfffd4efcb68`  
		Last Modified: Sat, 21 Dec 2019 04:01:10 GMT  
		Size: 1.9 MB (1870465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f452cbc16fa85ed90d6130ecf261e8e13fb0e25cee589b85be128a1593b97ee5`  
		Last Modified: Sat, 21 Dec 2019 07:40:29 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f92f62dabd77c43389196868563e1e6c9a244baf6584d401f5ebfcd344f8793`  
		Last Modified: Sat, 21 Dec 2019 07:40:29 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1358f54e3bffbfd101232d42f5bbd3a0034d243e7d569c882bb989ecb77e7d8`  
		Last Modified: Sat, 21 Dec 2019 07:42:14 GMT  
		Size: 127.3 MB (127319241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03a514e4a872694a5897d648742deb4c9b955344c9745b1017bc9449e31f2bc`  
		Last Modified: Sat, 21 Dec 2019 07:40:29 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; s390x

```console
$ docker pull plone@sha256:c2c914544d49d441436e73d9a2e7d4f9d1a9ee7c0e0c041244d8890bfc694833
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160708780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9523fb0fef2e9bb4e319be388515cd78f9a7f6ff015fbf482abb719e9bbc8177`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Mon, 21 Oct 2019 16:47:28 GMT
ADD file:49020543846e4f93b34d71c0e4234ade7bd6dde3f45cb73784aa73ce0522c8bc in / 
# Mon, 21 Oct 2019 16:47:29 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:57:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2019 18:57:49 GMT
ENV LANG=C.UTF-8
# Mon, 21 Oct 2019 18:57:51 GMT
RUN apk add --no-cache ca-certificates
# Mon, 21 Oct 2019 19:04:31 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Mon, 21 Oct 2019 19:04:32 GMT
ENV PYTHON_VERSION=3.7.5
# Fri, 15 Nov 2019 02:34:23 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 15 Nov 2019 02:34:24 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 15 Nov 2019 02:34:25 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 15 Nov 2019 02:34:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 15 Nov 2019 02:34:25 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 15 Nov 2019 02:34:30 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 15 Nov 2019 02:34:30 GMT
CMD ["python3"]
# Fri, 15 Nov 2019 04:42:50 GMT
ENV PIP=19.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=41.0.0 WHEEL=0.33.1 PLONE_MAJOR=5.2 PLONE_VERSION=5.2 PLONE_VERSION_RELEASE=5.2.0 PLONE_MD5=211ff749422611db2e448dea639e1fba
# Fri, 15 Nov 2019 04:42:50 GMT
LABEL plone=5.2 os=alpine os.version=3.10 name=Plone 5.2 description=Plone image, based on Unified Installer maintainer=Plone Community
# Fri, 15 Nov 2019 04:42:51 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 15 Nov 2019 04:42:51 GMT
COPY file:443d87cbc872ff84a1cc60cabe0940e8126ef435a982c2b29ffcc415ca0d5fd0 in /plone/instance/ 
# Fri, 15 Nov 2019 04:49:14 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/base_skeleton/* /plone/instance/ && cp -v ./Plone-$PLONE_VERSION_RELEASE-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo && rm -rf /plone/buildout-cache/downloads/*
# Fri, 15 Nov 2019 04:49:16 GMT
VOLUME [/data]
# Fri, 15 Nov 2019 04:49:16 GMT
COPY multi:c1f88121bdba3f4019314daa8a4906c592b99b3ebbde00413dc4680482b6d329 in / 
# Fri, 15 Nov 2019 04:49:16 GMT
EXPOSE 8080
# Fri, 15 Nov 2019 04:49:16 GMT
WORKDIR /plone/instance
# Fri, 15 Nov 2019 04:49:17 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 15 Nov 2019 04:49:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2019 04:49:17 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:fb7172052a60e640810f01efff381654bf9ed44082461455cfcc6306d192d541`  
		Last Modified: Mon, 21 Oct 2019 16:48:40 GMT  
		Size: 2.6 MB (2573587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306048a52bec4e296a3c1f47084b91102bca113f61ed7cff8b1f330e4e8b854b`  
		Last Modified: Tue, 22 Oct 2019 01:18:53 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b741c4eeb9e2b9973b8275a036a9f14a49e9604ab42239e5c75b33a326429`  
		Last Modified: Fri, 15 Nov 2019 03:59:02 GMT  
		Size: 29.0 MB (28984440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd321614ed3d378be64df57c45607a33062066562cc65b0e600bb83f8ce4414b`  
		Last Modified: Fri, 15 Nov 2019 03:58:55 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417901159e76193e6e3dd405cd541a68d07e4000d44df22ecb0ec78ecb3356a`  
		Last Modified: Fri, 15 Nov 2019 03:58:55 GMT  
		Size: 1.9 MB (1869027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b9f6f3fbbfe77b41d2c3f224b65bc947b01afbd373f79eb1faafca24678ba9`  
		Last Modified: Fri, 15 Nov 2019 05:49:59 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f233d6dcffb5912802b9c463d28784fbcf6bed31f4cb2a423844e8340b8fdb`  
		Last Modified: Fri, 15 Nov 2019 05:49:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5fdf41d499020aa3f9e9c5a0bebfd7fb850f14e5d79e99537bb9050430efff`  
		Last Modified: Fri, 15 Nov 2019 05:50:22 GMT  
		Size: 127.0 MB (126974124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31a2c8aaace186898557dbd6e64939ee8fce874250ce6944ba0a6b6e9b78658`  
		Last Modified: Fri, 15 Nov 2019 05:49:58 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
