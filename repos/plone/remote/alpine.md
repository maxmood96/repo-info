## `plone:alpine`

```console
$ docker pull plone@sha256:bbe3887775ed80154630bb06edc7b80417eb1e9ed837009f999c5173849c5783
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
$ docker pull plone@sha256:1abe06dc4ef8f00f0fd217370c9684929b0d722e8920ecadb68678e114b03e30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148735599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90d04f95ab5b57f6074a9339af7e7ea423bc2d154c690a97d4e89de1d5691e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 06:00:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 08:24:22 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 08:48:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 26 Mar 2021 08:48:59 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 08:48:59 GMT
ENV PYTHON_VERSION=3.8.8
# Fri, 26 Mar 2021 08:54:27 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 08:54:28 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 08:54:29 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 08:54:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 08:54:29 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 08:54:35 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 08:54:36 GMT
CMD ["python3"]
# Fri, 26 Mar 2021 21:13:49 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.4 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.4 PLONE_VERSION_RELEASE=Plone-5.2.4-UnifiedInstaller-1.0 PLONE_MD5=b682cdf2384e692c033077f448b68afd
# Fri, 26 Mar 2021 21:13:50 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 26 Mar 2021 21:13:50 GMT
COPY file:3ef405a950854449713102e91399f13c5d85d531f4bb6247863ee4357e81ed1c in /plone/instance/ 
# Fri, 26 Mar 2021 21:27:05 GMT
RUN apk add --no-cache --virtual .build-deps     build-base     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     mariadb-dev     openldap-dev     pcre-dev     postgresql-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     git     rsync     libxml2     libxslt     libjpeg-turbo     mariadb-connector-c     postgresql-client && rm -rf /plone/buildout-cache/downloads/*
# Fri, 26 Mar 2021 21:27:07 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 21:27:07 GMT
COPY multi:42ced57fe3a0905e0e2388d9f8e6e5bd32fb0db140cd61d93fb9326734196d09 in / 
# Fri, 26 Mar 2021 21:27:07 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 21:27:07 GMT
WORKDIR /plone/instance
# Fri, 26 Mar 2021 21:27:07 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 26 Mar 2021 21:27:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 21:27:08 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e34918dcd1d5a4999f8d084f1aed8b9b981a357cab20391ec352e2bf0a2c78`  
		Last Modified: Fri, 26 Mar 2021 09:28:56 GMT  
		Size: 281.3 KB (281260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c091c61c3dfab64d5aa33623c9854e3f6d5ecb0c92f0287a59b07d54b86982e`  
		Last Modified: Fri, 26 Mar 2021 09:28:57 GMT  
		Size: 11.2 MB (11192819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbbd84036ecdb6a4f0ef40bb14792b520415fceae5268cc92bace853c607612`  
		Last Modified: Fri, 26 Mar 2021 09:28:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9abdcd72c0531e40c0dc9e996d6393cebadbd1d682b85c54674e98d42fc0339`  
		Last Modified: Fri, 26 Mar 2021 09:28:56 GMT  
		Size: 2.2 MB (2164565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6d09cf49aba42b361f84330faa4711050070c7c73691e3ade2faa383b3683c`  
		Last Modified: Fri, 26 Mar 2021 21:27:48 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbc2b24b246e8b16f5fb92e765d43702b08ef1aa566ed0f5a7f4cd1b356b015`  
		Last Modified: Fri, 26 Mar 2021 21:27:48 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf03ca2d8396d53866a08084a126f6db2e9a1a751b204eef6fe57eeb74672e3e`  
		Last Modified: Fri, 26 Mar 2021 21:28:16 GMT  
		Size: 132.3 MB (132278622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1f2e874972a6c9e7db954187ad6a1ee4df4f9cbd293e4b1a2b8b7bff320180`  
		Last Modified: Fri, 26 Mar 2021 21:27:48 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm variant v6

```console
$ docker pull plone@sha256:123a658d76aabd9d1241a207ae65885356af334cfc0a7960d9005752a3eeb848
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147393529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f735214dc48198e59083bdffa6c3719700b88cd22de79b5e2e5b0b74b025ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 00:45:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 00:45:33 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 01:36:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Thu, 01 Apr 2021 01:36:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 01 Apr 2021 01:36:44 GMT
ENV PYTHON_VERSION=3.8.8
# Thu, 01 Apr 2021 01:46:57 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 01 Apr 2021 01:47:00 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 01 Apr 2021 01:47:01 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Thu, 01 Apr 2021 01:47:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Thu, 01 Apr 2021 01:47:03 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Thu, 01 Apr 2021 01:47:19 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 01 Apr 2021 01:47:21 GMT
CMD ["python3"]
# Thu, 01 Apr 2021 06:17:28 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.4 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.4 PLONE_VERSION_RELEASE=Plone-5.2.4-UnifiedInstaller-1.0 PLONE_MD5=b682cdf2384e692c033077f448b68afd
# Thu, 01 Apr 2021 06:17:31 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Thu, 01 Apr 2021 06:17:32 GMT
COPY file:3ef405a950854449713102e91399f13c5d85d531f4bb6247863ee4357e81ed1c in /plone/instance/ 
# Thu, 01 Apr 2021 06:40:41 GMT
RUN apk add --no-cache --virtual .build-deps     build-base     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     mariadb-dev     openldap-dev     pcre-dev     postgresql-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     git     rsync     libxml2     libxslt     libjpeg-turbo     mariadb-connector-c     postgresql-client && rm -rf /plone/buildout-cache/downloads/*
# Thu, 01 Apr 2021 06:40:49 GMT
VOLUME [/data]
# Thu, 01 Apr 2021 06:40:51 GMT
COPY multi:42ced57fe3a0905e0e2388d9f8e6e5bd32fb0db140cd61d93fb9326734196d09 in / 
# Thu, 01 Apr 2021 06:40:52 GMT
EXPOSE 8080
# Thu, 01 Apr 2021 06:40:52 GMT
WORKDIR /plone/instance
# Thu, 01 Apr 2021 06:40:53 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Thu, 01 Apr 2021 06:40:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 06:40:54 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900f11ca502dbd6a2339481720d4cebbc177442450c694cce2861d4b39dc8866`  
		Last Modified: Thu, 01 Apr 2021 02:55:13 GMT  
		Size: 281.4 KB (281445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34cdda08ef9d3423244c5bd8faa069689a9478885043d5c1ae9d1b278f95585`  
		Last Modified: Thu, 01 Apr 2021 02:55:19 GMT  
		Size: 10.8 MB (10770298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e22570740052aa2c457b64e1fdaed1f0a0eefafc288394906ccb21d73de71c`  
		Last Modified: Thu, 01 Apr 2021 02:55:14 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc32eaa233601961f1dbdd5eeabe0757b5fcec3896f7b2a7a7921993897eed5e`  
		Last Modified: Thu, 01 Apr 2021 02:55:14 GMT  
		Size: 2.2 MB (2164640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da728c187096a034f9ba70f7143ffe10cd6c00de6580cacb9e80e575e48814a4`  
		Last Modified: Thu, 01 Apr 2021 06:41:20 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6b332e1985c57040aa71a277c14fceadd650951f3d879d69cd8fd6e89226ae`  
		Last Modified: Thu, 01 Apr 2021 06:41:20 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d1105dbfabe443a930c88c5b43a53f8c4c197e210e4d4012bf46ae3e7d067`  
		Last Modified: Thu, 01 Apr 2021 06:42:10 GMT  
		Size: 131.5 MB (131548370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10497f3401932e717e86b2574b64b019afe4b489e5f65a6d333d2eaeaec3aac`  
		Last Modified: Thu, 01 Apr 2021 06:41:20 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; arm64 variant v8

```console
$ docker pull plone@sha256:3e7f08ae2f75da75174718e9c66c476cc93dd4bdb9ab22b1af3e275098880376
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148594761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a908161f587e601cbb6691ce6361d386e71135871753e3d6af39985ec694930`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 06:19:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 06:19:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 06:57:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 26 Mar 2021 06:57:15 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 06:57:17 GMT
ENV PYTHON_VERSION=3.8.8
# Fri, 26 Mar 2021 07:05:25 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 07:05:29 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 07:05:30 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 07:05:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 07:05:32 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 07:05:45 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 07:05:48 GMT
CMD ["python3"]
# Fri, 26 Mar 2021 18:51:59 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.4 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.4 PLONE_VERSION_RELEASE=Plone-5.2.4-UnifiedInstaller-1.0 PLONE_MD5=b682cdf2384e692c033077f448b68afd
# Fri, 26 Mar 2021 18:52:02 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 26 Mar 2021 18:52:03 GMT
COPY file:3ef405a950854449713102e91399f13c5d85d531f4bb6247863ee4357e81ed1c in /plone/instance/ 
# Fri, 26 Mar 2021 19:16:51 GMT
RUN apk add --no-cache --virtual .build-deps     build-base     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     mariadb-dev     openldap-dev     pcre-dev     postgresql-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     git     rsync     libxml2     libxslt     libjpeg-turbo     mariadb-connector-c     postgresql-client && rm -rf /plone/buildout-cache/downloads/*
# Fri, 26 Mar 2021 19:16:56 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 19:16:58 GMT
COPY multi:42ced57fe3a0905e0e2388d9f8e6e5bd32fb0db140cd61d93fb9326734196d09 in / 
# Fri, 26 Mar 2021 19:16:59 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 19:17:01 GMT
WORKDIR /plone/instance
# Fri, 26 Mar 2021 19:17:02 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 26 Mar 2021 19:17:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 19:17:04 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947ac8e6f45dd5d344c7edc30ca878be1f4ae70d9921cd88eba1113046e6ebf1`  
		Last Modified: Fri, 26 Mar 2021 08:06:08 GMT  
		Size: 281.5 KB (281484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfb4f27cd0d32313054c26ba532f221d5b38c345734c786d0adb636488bce80`  
		Last Modified: Fri, 26 Mar 2021 08:06:10 GMT  
		Size: 11.3 MB (11259516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63067e0ed558a7c1278e3b36691632d7721fa421c924cfc56cc6a30cbfc07ad`  
		Last Modified: Fri, 26 Mar 2021 08:06:08 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071ae32c5941201fd1a5fa90c68fcc50f21f6e9d052ad0100bc7c369e6be536a`  
		Last Modified: Fri, 26 Mar 2021 08:06:09 GMT  
		Size: 2.2 MB (2164647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a57ce5e4910e80914c94c408edfd5e2dc1eeed7bd15d9e3e8196eeb63371c9`  
		Last Modified: Fri, 26 Mar 2021 19:17:27 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d583ce04597cb39872d3c792f2f50c1ba3b2704e9cbdf69f8148af19cc50ec80`  
		Last Modified: Fri, 26 Mar 2021 19:17:27 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d623ad1b93aabde94788b93e5bcdaeed3af286908f779222a160a2f2c71cb265`  
		Last Modified: Fri, 26 Mar 2021 19:18:05 GMT  
		Size: 132.2 MB (132170564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1907190b1a0fd699be03cc3dfc4e9d32e4bb8792b7954a421822a0faf8f912`  
		Last Modified: Fri, 26 Mar 2021 19:17:27 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; 386

```console
$ docker pull plone@sha256:8557ab5c40fe9c7bdb2bf8b929a29dad97b098c2869b7f9404ba029212e02d10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66c07e049b8677a6e0f62a78dd491ff85aee7bb0c3233bf29cba86236c04c32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:13:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Mar 2021 18:13:59 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 19:05:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Wed, 31 Mar 2021 19:05:46 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Mar 2021 19:05:46 GMT
ENV PYTHON_VERSION=3.8.8
# Wed, 31 Mar 2021 19:18:47 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 31 Mar 2021 19:18:49 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 31 Mar 2021 19:18:49 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 31 Mar 2021 19:18:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Wed, 31 Mar 2021 19:18:50 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Wed, 31 Mar 2021 19:19:02 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 31 Mar 2021 19:19:02 GMT
CMD ["python3"]
# Wed, 31 Mar 2021 23:29:18 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.4 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.4 PLONE_VERSION_RELEASE=Plone-5.2.4-UnifiedInstaller-1.0 PLONE_MD5=b682cdf2384e692c033077f448b68afd
# Wed, 31 Mar 2021 23:29:19 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Wed, 31 Mar 2021 23:29:20 GMT
COPY file:3ef405a950854449713102e91399f13c5d85d531f4bb6247863ee4357e81ed1c in /plone/instance/ 
# Wed, 31 Mar 2021 23:52:17 GMT
RUN apk add --no-cache --virtual .build-deps     build-base     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     mariadb-dev     openldap-dev     pcre-dev     postgresql-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     git     rsync     libxml2     libxslt     libjpeg-turbo     mariadb-connector-c     postgresql-client && rm -rf /plone/buildout-cache/downloads/*
# Wed, 31 Mar 2021 23:52:19 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 23:52:20 GMT
COPY multi:42ced57fe3a0905e0e2388d9f8e6e5bd32fb0db140cd61d93fb9326734196d09 in / 
# Wed, 31 Mar 2021 23:52:21 GMT
EXPOSE 8080
# Wed, 31 Mar 2021 23:52:21 GMT
WORKDIR /plone/instance
# Wed, 31 Mar 2021 23:52:21 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Wed, 31 Mar 2021 23:52:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Mar 2021 23:52:22 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d68ce160b157cf435b47089adf11f7e42d535694161a2d5e5a7bb26277c1ddf`  
		Last Modified: Wed, 31 Mar 2021 23:09:13 GMT  
		Size: 281.8 KB (281814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27105dfb104f43b7d38031337df6af9360ed78e4b7f7673b25cd5ddd9a1072a2`  
		Last Modified: Wed, 31 Mar 2021 23:09:17 GMT  
		Size: 11.4 MB (11371874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1f9ed61250b8fee8cecb17b6917b41ae4e8441c4cff9e16b12781a193b5a76`  
		Last Modified: Wed, 31 Mar 2021 23:09:16 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384ca7c4120afe5cddd549ef9b9d66a075649837e6440366da61c1ac8a5a3c66`  
		Last Modified: Wed, 31 Mar 2021 23:09:14 GMT  
		Size: 2.2 MB (2164596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3590eaf575b50537dc62f4f1f7ebf9d450680863ee1ce1305ae92de0a66a7409`  
		Last Modified: Wed, 31 Mar 2021 23:53:00 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45ce1d130b55b84a241111cc1cf4bf262a89def31827ab2b16c73df6c83da8a`  
		Last Modified: Wed, 31 Mar 2021 23:53:00 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7960a6ef1ae1a55e545ab5001aa329724331acc0e4e24471e3622907a8299108`  
		Last Modified: Wed, 31 Mar 2021 23:53:57 GMT  
		Size: 133.3 MB (133300700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16c91a7f62beee07e1cbd900d0cb415fde794c23c137f804dfa2d8a2078ee`  
		Last Modified: Wed, 31 Mar 2021 23:53:01 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; ppc64le

```console
$ docker pull plone@sha256:6777103952b064902e97f9f24bd762e51aa10d7a669aa1054f965cb44358e7e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150298969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb51b82bbe244396dd9a184f3020edf4b227193bdd621a4f6e7316d4c468cfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Thu, 25 Mar 2021 22:22:28 GMT
ADD file:f91f8e0aa646cb847f6e210056280f9332382ad2f8d6a8839fd9aa69b81c4a2a in / 
# Thu, 25 Mar 2021 22:22:30 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:26:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 02:27:05 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 22:40:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 26 Mar 2021 22:40:22 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 22:40:24 GMT
ENV PYTHON_VERSION=3.8.8
# Fri, 26 Mar 2021 22:48:37 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 22:48:47 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 22:48:50 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 22:48:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 22:48:56 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 22:49:16 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 22:49:19 GMT
CMD ["python3"]
# Sun, 28 Mar 2021 00:03:25 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.4 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.4 PLONE_VERSION_RELEASE=Plone-5.2.4-UnifiedInstaller-1.0 PLONE_MD5=b682cdf2384e692c033077f448b68afd
# Sun, 28 Mar 2021 00:03:38 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sun, 28 Mar 2021 00:03:41 GMT
COPY file:3ef405a950854449713102e91399f13c5d85d531f4bb6247863ee4357e81ed1c in /plone/instance/ 
# Sun, 28 Mar 2021 00:24:54 GMT
RUN apk add --no-cache --virtual .build-deps     build-base     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     mariadb-dev     openldap-dev     pcre-dev     postgresql-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     git     rsync     libxml2     libxslt     libjpeg-turbo     mariadb-connector-c     postgresql-client && rm -rf /plone/buildout-cache/downloads/*
# Sun, 28 Mar 2021 00:25:06 GMT
VOLUME [/data]
# Sun, 28 Mar 2021 00:25:10 GMT
COPY multi:42ced57fe3a0905e0e2388d9f8e6e5bd32fb0db140cd61d93fb9326734196d09 in / 
# Sun, 28 Mar 2021 00:25:14 GMT
EXPOSE 8080
# Sun, 28 Mar 2021 00:25:18 GMT
WORKDIR /plone/instance
# Sun, 28 Mar 2021 00:25:22 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sun, 28 Mar 2021 00:25:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Mar 2021 00:25:33 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:f3b2866c25f0a9167af050d646a7a740ccc88d46e068c90ff28a5c2ec2ee0030`  
		Last Modified: Thu, 25 Mar 2021 22:24:08 GMT  
		Size: 2.8 MB (2813115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5947c0e62afc347d4f9ef3c52d2dbe2952b28e074f4800f0d2b96827294b04fd`  
		Last Modified: Sat, 27 Mar 2021 00:59:24 GMT  
		Size: 283.4 KB (283404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bade8747a639b7a3b2f7ac2c51d49215a797ca96e0b58f83e7738689d919288d`  
		Last Modified: Sat, 27 Mar 2021 00:59:27 GMT  
		Size: 11.5 MB (11485635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059fa823fbbe3486e6eaa09a9f61547bf3d47f1e3c22fcccb3bf99f2a284329`  
		Last Modified: Sat, 27 Mar 2021 00:59:24 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0927ef77437933562c4564e97c4ca9565758946f6800be5acd2841961db47de`  
		Last Modified: Sat, 27 Mar 2021 00:59:25 GMT  
		Size: 2.2 MB (2164709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16443e88409ec88bc896821e8ea75b78b5dcbeb5ae8e189587a71ed6a90e10a`  
		Last Modified: Sun, 28 Mar 2021 00:26:00 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987c3ef081e671af1e518a32a3e9305e8d4d4aeac79f9ca43ac326fbf0e0871`  
		Last Modified: Sun, 28 Mar 2021 00:25:59 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f5db8281c67f22151a90c599c042ea7fe2cdc3a29ad24212706008a07915b3`  
		Last Modified: Sun, 28 Mar 2021 00:26:29 GMT  
		Size: 133.5 MB (133545437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d23b664a21a3e9e135e03b350c9587f97851d68c7a728304146a70acc1dd72c`  
		Last Modified: Sun, 28 Mar 2021 00:25:59 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:alpine` - linux; s390x

```console
$ docker pull plone@sha256:f530af783a2e4cf2cec15dd8d4cf1e3cd478286c297db0196aa67d4830e96cec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148365612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a053482f5bc43a8e7b16257d0bc74cfbf25e27ab37697800242a19c838502b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Mar 2021 17:14:58 GMT
ADD file:3f5fe04867af3c9f2cfc5b315d97097145ae11343399985386321a8db21d7786 in / 
# Wed, 31 Mar 2021 17:14:58 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 02:52:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 02:52:47 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 03:17:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Thu, 01 Apr 2021 03:17:46 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 01 Apr 2021 03:17:47 GMT
ENV PYTHON_VERSION=3.8.8
# Thu, 01 Apr 2021 03:22:57 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 01 Apr 2021 03:22:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 01 Apr 2021 03:23:00 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Thu, 01 Apr 2021 03:23:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Thu, 01 Apr 2021 03:23:00 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Thu, 01 Apr 2021 03:23:07 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 01 Apr 2021 03:23:07 GMT
CMD ["python3"]
# Thu, 01 Apr 2021 05:50:36 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.4 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.4 PLONE_VERSION_RELEASE=Plone-5.2.4-UnifiedInstaller-1.0 PLONE_MD5=b682cdf2384e692c033077f448b68afd
# Thu, 01 Apr 2021 05:50:37 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Thu, 01 Apr 2021 05:50:38 GMT
COPY file:3ef405a950854449713102e91399f13c5d85d531f4bb6247863ee4357e81ed1c in /plone/instance/ 
# Thu, 01 Apr 2021 06:01:47 GMT
RUN apk add --no-cache --virtual .build-deps     build-base     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     mariadb-dev     openldap-dev     pcre-dev     postgresql-dev     libffi-dev && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz && echo "$PLONE_MD5  Plone.tgz" | md5sum -c - && tar -zxvf Plone.tgz && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/ && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL && cd /plone/instance && buildout && ln -s /data/filestorage/ /plone/instance/var/filestorage && ln -s /data/blobstorage /plone/instance//var/blobstorage && find /data  -not -user plone -exec chown plone:plone {} \+ && find /plone -not -user plone -exec chown plone:plone {} \+ && rm -rf /Plone* && apk del .build-deps && apk add --no-cache --virtual .run-deps     su-exec     bash     git     rsync     libxml2     libxslt     libjpeg-turbo     mariadb-connector-c     postgresql-client && rm -rf /plone/buildout-cache/downloads/*
# Thu, 01 Apr 2021 06:02:15 GMT
VOLUME [/data]
# Thu, 01 Apr 2021 06:02:15 GMT
COPY multi:42ced57fe3a0905e0e2388d9f8e6e5bd32fb0db140cd61d93fb9326734196d09 in / 
# Thu, 01 Apr 2021 06:02:15 GMT
EXPOSE 8080
# Thu, 01 Apr 2021 06:02:16 GMT
WORKDIR /plone/instance
# Thu, 01 Apr 2021 06:02:17 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Thu, 01 Apr 2021 06:02:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 06:02:18 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:1d4058bbeedf5296bcaf5ae8f37c8cd58152acad3ec45a536e08b83f5d3abe83`  
		Last Modified: Wed, 31 Mar 2021 17:15:36 GMT  
		Size: 2.6 MB (2602591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fffd1159bc5cc1fd5bd07c481c7b17f9ed5edeee2ef0f68ced35a80e9c7faa`  
		Last Modified: Thu, 01 Apr 2021 03:54:30 GMT  
		Size: 281.7 KB (281695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805c9e9fab14a2415364900a5f9edfcb3e6132e0ef247b5b665b98d55f864e0d`  
		Last Modified: Thu, 01 Apr 2021 03:54:31 GMT  
		Size: 11.2 MB (11174524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de8d49298d1eafe446ad5b89dcecaa5dd1a86f46d6214a44cad057bd665ddb`  
		Last Modified: Thu, 01 Apr 2021 03:54:30 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce27955515b43cb8a3c2e314caafd5b908b854043b8752fbed87db2f452500`  
		Last Modified: Thu, 01 Apr 2021 03:54:30 GMT  
		Size: 2.2 MB (2164538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f6d7a5020353f7afdcbbd2f5d9ba51bad83a164145f4fdf7208ec70c5de93`  
		Last Modified: Thu, 01 Apr 2021 06:02:32 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6ecb33d431c9945275e6c5841b7e3b42e63ecb5fd9450d2eb41a52dd6647ee`  
		Last Modified: Thu, 01 Apr 2021 06:02:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e330170bab8fc4bb0a89b920f86c57991d064ea956c0b9fcdc51f353089b0c5`  
		Last Modified: Thu, 01 Apr 2021 06:02:52 GMT  
		Size: 132.1 MB (132135607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a7a25c667e84b12c000e660b9dae1d45c708df978461e8442e4b94ab6dd40`  
		Last Modified: Thu, 01 Apr 2021 06:02:33 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
