## `plone:python38`

```console
$ docker pull plone@sha256:e73ae6e9864e43d4d49169f9fda09012d48c7720e8e204a8b0304b764600923b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:python38` - linux; amd64

```console
$ docker pull plone@sha256:73b00cd4bbefdbe229f1395a42b521aab0f3fe38c7b464437ed991853ac489e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325c561650f0abe55f3f62776ff3433f7c5e0c625bc0c030a983357540a8103b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70db9fc16b3a82cf692a0638d1eb07a4ba059d51c2f2b64953ca3b9a7a946bff`  
		Last Modified: Fri, 27 Sep 2024 06:05:35 GMT  
		Size: 1.1 MB (1076283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d245b2373f6348d372d085cf82f87d57503110b94bd1b7c73d5689e103052e0f`  
		Last Modified: Fri, 27 Sep 2024 06:05:35 GMT  
		Size: 13.7 MB (13681722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d01992d34a6a249cc367476cb878274d4b9ecdd6d02e72d39f7a7b3fcc1899`  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcd4679655c8a5448fced2294bc16c7ef47c7fad654a55e9de28ce19bea18dd`  
		Last Modified: Fri, 27 Sep 2024 07:32:10 GMT  
		Size: 3.8 KB (3805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5145bd0b186a9f36f74bdd83af9edc4a7b7571cf9f344f51bca3631550bad40f`  
		Last Modified: Fri, 27 Sep 2024 07:32:10 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c42bd328d53a1645886cf0f0327677b7a7788967f1804ab00770456b06e0cc`  
		Last Modified: Fri, 27 Sep 2024 07:32:16 GMT  
		Size: 223.0 MB (222955501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84151f1513a6de0783586d0b1648f7da72f60c29eaf3993c52b12580e97eb3c`  
		Last Modified: Fri, 27 Sep 2024 07:32:10 GMT  
		Size: 4.0 KB (4024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:python38` - unknown; unknown

```console
$ docker pull plone@sha256:8a80e12a42f5b35700ec52199ca5828ab3ab5a63c647413e5acb3eb408ec242e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464564db863726aa9b4ac4f77a3013afc330de761a4fa5cbd0974003b9aab9a8`

```dockerfile
```

-	Layers:
	-	`sha256:33a1690ae9d56f1c01da75c2a303b25d86d8cd6a601102bdc2a0f8048a8bb27b`  
		Size: 7.2 MB (7151114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b001a8496960aed6c659d3350c88d46410195d50f62b96a362efc6125c49684`  
		Last Modified: Fri, 27 Sep 2024 07:32:10 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json
