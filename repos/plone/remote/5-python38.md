## `plone:5-python38`

```console
$ docker pull plone@sha256:7dba3d37f32ac0ac58de553a115fdc97d1905d03b3213a50a7b7b63594e485b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `plone:5-python38` - linux; amd64

```console
$ docker pull plone@sha256:172b4c7f504a06d96a767afda6966956f1674451a12ee0dbc20a4ea1c80addda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274012010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e17786e84a5088e5d7a645bc94a2a4b95257c262aa592b96c62b35496d186b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Wed, 31 Jul 2024 10:13:39 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2386629653d943478ada3d6e0a3dac41c2928a140fc0d52603cfe68f6735e78d`  
		Last Modified: Wed, 04 Sep 2024 06:06:08 GMT  
		Size: 1.1 MB (1076283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5bfa4da4c65fdd0e3629edcd62ddda04e1769310bb7655f3e467efe254ecd`  
		Last Modified: Wed, 04 Sep 2024 06:06:09 GMT  
		Size: 15.8 MB (15765745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017d2e3149f354e8da7495e1e3c483ea2131969cdd48d6a8bfb4f29df6d5990`  
		Last Modified: Wed, 04 Sep 2024 06:06:08 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9516a3ac8e8e22b24a9fe0c1aa77be8dddc7605cd9fc30b25107f3d0f2706`  
		Last Modified: Wed, 04 Sep 2024 06:06:08 GMT  
		Size: 2.8 MB (2775231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bff77e5f1c551d6f2178abef41bc2e888c295989dd43633faac237aa944c8`  
		Last Modified: Wed, 04 Sep 2024 07:19:39 GMT  
		Size: 3.8 KB (3813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cf38cdbb71be8150f508923c4409d2a4d8b2ef66dc2b96d84dd719d0ebb5ef`  
		Last Modified: Wed, 04 Sep 2024 07:19:39 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684059002757dbf0e7c83c720a3024813d022765a15da7494934b40910febebd`  
		Last Modified: Wed, 04 Sep 2024 07:19:43 GMT  
		Size: 223.0 MB (222957117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10ff1b79b07d705eb65edf29fae72d6a65c6922268632e1bec64d3ede3f163`  
		Last Modified: Wed, 04 Sep 2024 07:19:39 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `plone:5-python38` - unknown; unknown

```console
$ docker pull plone@sha256:bb705b28de716c97e4f9ea9cdfed7932fe6d1a3f3654895eea600f2b154d5652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6d29522626b8693a5d6b6208e628dce688aa5d9c6b8590c14b62ce4cad8582`

```dockerfile
```

-	Layers:
	-	`sha256:6f185159aa68b5e6da70cec2c102662882256079e401378e0a9f7a3183ec2ca6`  
		Last Modified: Wed, 04 Sep 2024 07:19:39 GMT  
		Size: 7.2 MB (7152320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a58fa44ce07fd85bf20b61bdeaaba8ae55a92e1d1a623ca38b3e252e08b6dd`  
		Last Modified: Wed, 04 Sep 2024 07:19:39 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json
