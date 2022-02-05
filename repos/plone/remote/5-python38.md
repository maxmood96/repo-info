## `plone:5-python38`

```console
$ docker pull plone@sha256:0c9e14c96a9d33d7fec8747d7414769ddaee9405a445e776e04e6299429b62f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `plone:5-python38` - linux; amd64

```console
$ docker pull plone@sha256:f9b84b413a30645a2c46327d687488abeb3c2e482f1eac4d99e69bccae88b7d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243286787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6c0d78f75710f3254145f7844ebecf0c68007b94656d656ec4d865e3e3108f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 20:36:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 20:36:00 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 20:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 21:15:16 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 29 Jan 2022 05:26:04 GMT
ENV PYTHON_VERSION=3.8.12
# Sat, 29 Jan 2022 05:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 	cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Sat, 29 Jan 2022 05:35:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Sat, 29 Jan 2022 05:35:24 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 29 Jan 2022 05:35:25 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 04 Feb 2022 23:23:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Fri, 04 Feb 2022 23:23:33 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Fri, 04 Feb 2022 23:23:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	; 	rm -f get-pip.py
# Fri, 04 Feb 2022 23:23:45 GMT
CMD ["python3"]
# Sat, 05 Feb 2022 06:09:07 GMT
ENV PIP=21.0.1 ZC_BUILDOUT=2.13.5 SETUPTOOLS=51.3.3 WHEEL=0.36.2 PLONE_MAJOR=5.2 PLONE_VERSION=5.2.7 PLONE_VERSION_RELEASE=Plone-5.2.7-UnifiedInstaller-1.0 PLONE_MD5=c180d7ce3170b1871a7e8d53938096b1
# Sat, 05 Feb 2022 06:09:08 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /plone/instance/ /data/filestorage /data/blobstorage
# Sat, 05 Feb 2022 06:09:09 GMT
COPY file:7b22c8ff5914ecee959543c0622bbb71de3b59961836e6f0bad3c41c35197e25 in /plone/instance/ 
# Sat, 05 Feb 2022 06:13:17 GMT
RUN buildDeps="default-libmysqlclient-dev dpkg-dev gcc libbz2-dev libc6-dev libffi-dev libjpeg62-turbo-dev libldap2-dev libopenjp2-7-dev libpcre3-dev libpq-dev libsasl2-dev libssl-dev libtiff5-dev libxml2-dev libxslt1-dev wget zlib1g-dev"  && runDeps="default-libmysqlclient-dev git gosu libjpeg62 libopenjp2-7 libpq5 libtiff5 libxml2 libxslt1.1 lynx netcat poppler-utils rsync wv"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/$PLONE_VERSION_RELEASE.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && cp -rv ./$PLONE_VERSION_RELEASE/base_skeleton/* /plone/instance/  && cp -v ./$PLONE_VERSION_RELEASE/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance/var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*
# Sat, 05 Feb 2022 06:13:20 GMT
VOLUME [/data]
# Sat, 05 Feb 2022 06:13:21 GMT
COPY multi:cb7e252b86bd636999944f95a07a275ae82b4f8eefb11a49319425c7445203ac in / 
# Sat, 05 Feb 2022 06:13:21 GMT
EXPOSE 8080
# Sat, 05 Feb 2022 06:13:21 GMT
WORKDIR /plone/instance
# Sat, 05 Feb 2022 06:13:21 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 05 Feb 2022 06:13:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:13:22 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4887dad22fda8ead06b653271b8a6fde0f36b5d8aaa804f12f79a0fef138de5`  
		Last Modified: Wed, 26 Jan 2022 22:34:52 GMT  
		Size: 2.8 MB (2770186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcccbd80a1adc59bf0d5a7ff05c5806afa8417c9ca3b87914b9e2ac755b0812`  
		Last Modified: Sat, 29 Jan 2022 06:54:11 GMT  
		Size: 10.7 MB (10728843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0995a517cdf86ed3b8c1183c9f52caadc88aaa532bc15953e1c8f25df2e0d478`  
		Last Modified: Sat, 29 Jan 2022 06:54:09 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f8ebb650996618103f082c6713ea911de68b52a9375bf07e85e3586d192c92`  
		Last Modified: Fri, 04 Feb 2022 23:32:47 GMT  
		Size: 2.6 MB (2642766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4270db0db0af7de0f0c2d211c1b7c4edbdc121fbba42e932ef2cd4bbf0bbaf`  
		Last Modified: Sat, 05 Feb 2022 06:22:02 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b84fcafd098303d138042f367f2efa208557e9bd2a9f25d05a20e1f038f7c8`  
		Last Modified: Sat, 05 Feb 2022 06:22:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b63a1ff29ca2404ab292db3e733650c545da7d86dd3093dfebb59d18bb3075`  
		Last Modified: Sat, 05 Feb 2022 06:22:32 GMT  
		Size: 200.0 MB (199981805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935cdb80d8683d57b53417c55d9628212d8167a47ccd65f3d72323193bacc135`  
		Last Modified: Sat, 05 Feb 2022 06:22:02 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
