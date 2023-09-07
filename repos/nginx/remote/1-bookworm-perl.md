## `nginx:1-bookworm-perl`

```console
$ docker pull nginx@sha256:f184cca81c35a018903aba05d20f4bba164c885d299d3423b9043f85fd35d54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `nginx:1-bookworm-perl` - linux; amd64

```console
$ docker pull nginx@sha256:a5241d68d1c2d614dd248cdf03653983421638afd0e6570e697488ac89ed4ae4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82293058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a465b9c519a059770cc3d5a7376ce866ee6009adaf3de30310f0765a793ae274`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:46 GMT
ADD file:997f5a9b32407d96efac41a1cfafb318f77de077c8b5cd7065b6ec9796b4bf5e in / 
# Wed, 16 Aug 2023 00:59:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 09:50:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Aug 2023 09:50:33 GMT
ENV NGINX_VERSION=1.25.2
# Wed, 16 Aug 2023 09:50:33 GMT
ENV NJS_VERSION=0.8.0
# Wed, 16 Aug 2023 09:50:33 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Aug 2023 09:50:54 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 16 Aug 2023 09:50:55 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 16 Aug 2023 09:50:55 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 09:50:55 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 09:50:55 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 09:50:55 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 09:50:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 09:50:55 GMT
EXPOSE 80
# Wed, 16 Aug 2023 09:50:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Aug 2023 09:50:55 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 16 Aug 2023 09:51:12 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:52d2b7f179e32b4cbd579ee3c4958027988f9a8274850ab0c7c24661e3adaac5`  
		Last Modified: Wed, 16 Aug 2023 01:04:30 GMT  
		Size: 29.1 MB (29124563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f026c631046113bd492f69761c3ba6042c791c35a60e7c7f3b8f254592daa`  
		Last Modified: Wed, 16 Aug 2023 09:52:52 GMT  
		Size: 41.3 MB (41338560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055fa98b43638b67d10c58d41094d99c8696cc34b7a960c7a0cc5d9d152d12b3`  
		Last Modified: Wed, 16 Aug 2023 09:52:44 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96576293dd2954ff84251aa0455687c8643358ba1b190ea1818f56b41884bdbd`  
		Last Modified: Wed, 16 Aug 2023 09:52:44 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c4092be9044bd4eef78f27c95785ef3a9f345d01fd4512bc94ddaaefc359f4`  
		Last Modified: Wed, 16 Aug 2023 09:52:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b6889c89547ec9ba653ab44ed32a99370940d51df956968c0d578dd61ab665`  
		Last Modified: Wed, 16 Aug 2023 09:52:44 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da761d9a302b21dc50767b67d46f737f5072fb4490c525b4a7ae6f18e1dbbf75`  
		Last Modified: Wed, 16 Aug 2023 09:52:44 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c2235cc8b6b4cac94fd8fff7d4ca689d7ee2c5850ab9f5029ce19b56ec8fec`  
		Last Modified: Wed, 16 Aug 2023 09:53:19 GMT  
		Size: 11.8 MB (11825359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:f002f0f0d1307466bb618cd6b375efa7c960c4fa223eb2e3c42fb5322562a0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74529255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aaa5f258696d8dff26d691997831b748fcc0468badb72b058d3ac77025fc0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Aug 2023 23:48:32 GMT
ADD file:661e14e9730f2608fba590f84fbb357838a3068db018f1e0569c79035783c86d in / 
# Tue, 15 Aug 2023 23:48:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:38:18 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Aug 2023 07:38:18 GMT
ENV NGINX_VERSION=1.25.2
# Wed, 16 Aug 2023 07:38:18 GMT
ENV NJS_VERSION=0.8.0
# Wed, 16 Aug 2023 07:38:18 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Aug 2023 07:42:10 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 16 Aug 2023 07:42:10 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 16 Aug 2023 07:42:10 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 07:42:11 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 07:42:11 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 07:42:11 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 07:42:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 07:42:11 GMT
EXPOSE 80
# Wed, 16 Aug 2023 07:42:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Aug 2023 07:42:11 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 16 Aug 2023 07:43:24 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:46d4cdda07fa660f92a3251737b0b22ad71ebafb783af374930d636935a2d8eb`  
		Last Modified: Tue, 15 Aug 2023 23:51:34 GMT  
		Size: 27.0 MB (26983543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef434c2d40400ad250493389cc7028fdff3663d255a6f02eb83ad9cb78506ca`  
		Last Modified: Wed, 16 Aug 2023 07:48:45 GMT  
		Size: 36.2 MB (36170287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d958148c14b5f58b4d6da4f4ad2c407b73c56f452248eb1c0157f526e446fde`  
		Last Modified: Wed, 16 Aug 2023 07:48:37 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1553cc1fb9d994d9343a8caebfc7ec44061e8e127a099082b49063eae0648c`  
		Last Modified: Wed, 16 Aug 2023 07:48:38 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b622c14fe4269759c815d887063f3907035649fc2e6c18696074df56a398d0c`  
		Last Modified: Wed, 16 Aug 2023 07:48:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e786a4b7548abc14cb50a100492d703361dab853047298f9fd2678d0e4e43526`  
		Last Modified: Wed, 16 Aug 2023 07:48:38 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8976743405a06b153ea746668bc63d9350e6156c72c0191a6dc6517896a17681`  
		Last Modified: Wed, 16 Aug 2023 07:48:37 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caabe0aca26bbd0f81176c054f0cb1ffe5b3b2334c542efff2f488ba2d96d50`  
		Last Modified: Wed, 16 Aug 2023 07:49:13 GMT  
		Size: 11.4 MB (11370847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:1b349186627915ce2ff2caa6d5ef5288a18983463c2cf0a44bd5139809b03426
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70683448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e94f6e4baec55d5523bf33faae21b409c2661edbad93d1dca362d377ade612d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 07 Sep 2023 00:57:48 GMT
ADD file:5775cb975a13a9e48198190564cd469f115a433dabc5c3406c45e1ef0b1ccdf0 in / 
# Thu, 07 Sep 2023 00:57:49 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:46:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 07 Sep 2023 03:46:36 GMT
ENV NGINX_VERSION=1.25.2
# Thu, 07 Sep 2023 03:46:36 GMT
ENV NJS_VERSION=0.8.0
# Thu, 07 Sep 2023 03:46:36 GMT
ENV PKG_RELEASE=1~bookworm
# Thu, 07 Sep 2023 03:50:33 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 07 Sep 2023 03:50:33 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Thu, 07 Sep 2023 03:50:33 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 03:50:33 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 03:50:33 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 03:50:33 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 03:50:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:50:34 GMT
EXPOSE 80
# Thu, 07 Sep 2023 03:50:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 Sep 2023 03:50:34 GMT
CMD ["nginx" "-g" "daemon off;"]
# Thu, 07 Sep 2023 03:51:36 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:6a9fec8868f77cdcda1bf847be168c1d104031ca6c8edc961bc7f76e3a4bf54b`  
		Last Modified: Thu, 07 Sep 2023 01:02:31 GMT  
		Size: 24.8 MB (24805221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133d4d525c9d0e0c3ae46634be6576b3f371221b7c96c71b5ca2191b5807bf8b`  
		Last Modified: Thu, 07 Sep 2023 03:57:33 GMT  
		Size: 34.7 MB (34703699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2fd0e866a7c8b8edd5c2196c376b45c074823df75b217df6ce49dc347cae4f`  
		Last Modified: Thu, 07 Sep 2023 03:57:26 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8455857999dd40fa363511b5c6e1523b8d576e7f467341c4df6bf06b33519da5`  
		Last Modified: Thu, 07 Sep 2023 03:57:26 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5352ddc4543088ab8d72bb77225d36e23ee3e48e6c347b2ed6e3d60cd15cfed`  
		Last Modified: Thu, 07 Sep 2023 03:57:26 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc052916d6848cbb1233ad2c8fbacf0df6b4ed9a0a043959abc8ec1acfa01a1`  
		Last Modified: Thu, 07 Sep 2023 03:57:26 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf49b881797ce3e121be09f006e83b462e22e06893987adf2b11f58f18880875`  
		Last Modified: Thu, 07 Sep 2023 03:57:26 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb90ace92a8c6ce665fd45015d7191bb9a8946ab57c8b22e35c65b91a9438214`  
		Last Modified: Thu, 07 Sep 2023 03:58:03 GMT  
		Size: 11.2 MB (11169950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:0faf542a79074349785dc1a6657eefb3a471b122015b5a5380712eeef32db1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78967238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cedd626f3165b1c97357da709f3cc025548c4893b4a6153ef6e331763cf7e00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:39 GMT
ADD file:fb5c8f411c4a1e06c25ac32455221938386907d0b4782fc228ca67de63a7e9de in / 
# Thu, 07 Sep 2023 00:39:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:30:40 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 07 Sep 2023 06:30:40 GMT
ENV NGINX_VERSION=1.25.2
# Thu, 07 Sep 2023 06:30:40 GMT
ENV NJS_VERSION=0.8.0
# Thu, 07 Sep 2023 06:30:40 GMT
ENV PKG_RELEASE=1~bookworm
# Thu, 07 Sep 2023 06:31:00 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 07 Sep 2023 06:31:00 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Thu, 07 Sep 2023 06:31:00 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:31:00 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:31:00 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:31:01 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:31:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:31:01 GMT
EXPOSE 80
# Thu, 07 Sep 2023 06:31:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 Sep 2023 06:31:01 GMT
CMD ["nginx" "-g" "daemon off;"]
# Thu, 07 Sep 2023 06:31:13 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:155eab17d86c47443adc8cebe7fc62c847c03db8cfb1ca53aa6276564fff23ef`  
		Last Modified: Thu, 07 Sep 2023 00:43:02 GMT  
		Size: 29.2 MB (29157149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b890a6ab7ff7b8857e7518391c55a07c00f08354ce15022747b04c7480c5ecaa`  
		Last Modified: Thu, 07 Sep 2023 06:32:37 GMT  
		Size: 38.0 MB (38016686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edde10874f477802543cbfc2667cbf6d951765a8457b506c5b8c5dc9aaa1253e`  
		Last Modified: Thu, 07 Sep 2023 06:32:31 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1969d2f2b2a3c59a01b1c42a037283d54fb39b1ec47b240e6488cd7bebd6808`  
		Last Modified: Thu, 07 Sep 2023 06:32:31 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983d8b18b7dedc63724164ba444a30fcdacd8de319a54be046366041cb476427`  
		Last Modified: Thu, 07 Sep 2023 06:32:31 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d0a268cf0b818c5e265d08837868cf0fa10684bed2e42c1a2dc3085e643049`  
		Last Modified: Thu, 07 Sep 2023 06:32:31 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff51b8992c4c660adbc30c6e92ae07102634998d9ed557e15d83d6f8e2c5b08`  
		Last Modified: Thu, 07 Sep 2023 06:32:31 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a10e1ecc32b98a27930b245eae1bf8439d25f453f905f2a3ba5e6b285c6533`  
		Last Modified: Thu, 07 Sep 2023 06:33:04 GMT  
		Size: 11.8 MB (11788831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; 386

```console
$ docker pull nginx@sha256:52d5b096563041fb77016b181be805c75df692814c81887bd076bf506373004c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80219386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1647f6f24d04312763d9b4191f3dd3c7e9177808243c01d4e37f1a34c4f008e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:01 GMT
ADD file:ffdb2f26091492ac2e82793b461bb70da9ce1d68d219ec0db182b4510e82586b in / 
# Tue, 15 Aug 2023 23:39:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:01:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Aug 2023 00:01:39 GMT
ENV NGINX_VERSION=1.25.2
# Wed, 16 Aug 2023 00:01:39 GMT
ENV NJS_VERSION=0.8.0
# Wed, 16 Aug 2023 00:01:39 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Aug 2023 00:06:46 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 16 Aug 2023 00:06:47 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 16 Aug 2023 00:06:47 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 00:06:47 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 00:06:47 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 00:06:47 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 00:06:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 00:06:47 GMT
EXPOSE 80
# Wed, 16 Aug 2023 00:06:47 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Aug 2023 00:06:48 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 16 Aug 2023 00:08:00 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:a12cc43de7614ac71c57865601eb4cedd27ce910b66c5091e07781b8547d5b0b`  
		Last Modified: Tue, 15 Aug 2023 23:43:26 GMT  
		Size: 30.1 MB (30141823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ae44115289309cb822129ee1f40b60752e7412d962128267483369851f13e`  
		Last Modified: Wed, 16 Aug 2023 00:19:30 GMT  
		Size: 38.5 MB (38480502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3264ca8dc8d5077004ae8381d5c2b70f404c937a3c4faaee0737692ac747ea27`  
		Last Modified: Wed, 16 Aug 2023 00:19:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4674c5981269d5d02c1495bf19786bac7cb21c58f76a74e4c1938aa7a0bb030c`  
		Last Modified: Wed, 16 Aug 2023 00:19:21 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d3c923ac69ec87cd16295e4f6c123fc8041a28c9eb668eca1fc2096dbfb1cb`  
		Last Modified: Wed, 16 Aug 2023 00:19:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89423fc4bd77cbe6a5ab13e7211b0e0f0ed10ab081cb768340f3cbe70e16e50`  
		Last Modified: Wed, 16 Aug 2023 00:19:21 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a013a1dee05c0182bda3a24abe839cda1067d2cd9eb8dbdedc6b0a0301335f13`  
		Last Modified: Wed, 16 Aug 2023 00:19:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2719b2c6b9eaed6e9442c03fe03a448ee8d86c6d455a07c1cb2cc8745ca76b3c`  
		Last Modified: Wed, 16 Aug 2023 00:20:00 GMT  
		Size: 11.6 MB (11592486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:2a8824c8bdc81f63a7cca2c714cdb8ab3f83fc94b475da62ac473cc21999e40c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dcf7c07b2099c9c176ea5ff76c6744192bfe7fcd8e5d64653635bc9f475e6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Aug 2023 00:08:43 GMT
ADD file:6122efd66f4e010b48e48eeb243d900439ef783f5a10df76043546a288d35d38 in / 
# Wed, 16 Aug 2023 00:08:47 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 21:59:07 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 17 Aug 2023 21:59:10 GMT
ENV NGINX_VERSION=1.25.2
# Thu, 17 Aug 2023 21:59:13 GMT
ENV NJS_VERSION=0.8.0
# Thu, 17 Aug 2023 21:59:15 GMT
ENV PKG_RELEASE=1~bookworm
# Thu, 17 Aug 2023 22:17:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 17 Aug 2023 22:17:20 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Thu, 17 Aug 2023 22:17:22 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Thu, 17 Aug 2023 22:17:24 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Thu, 17 Aug 2023 22:17:26 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Thu, 17 Aug 2023 22:17:28 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Thu, 17 Aug 2023 22:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 22:17:33 GMT
EXPOSE 80
# Thu, 17 Aug 2023 22:17:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Aug 2023 22:17:39 GMT
CMD ["nginx" "-g" "daemon off;"]
# Thu, 17 Aug 2023 22:22:21 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:52390931db742e6fb36945aff79b92fea76dcfe0964f8a5cf7e5b5faaa40b80f`  
		Last Modified: Wed, 16 Aug 2023 00:19:34 GMT  
		Size: 29.1 MB (29121481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37a74eef2c1f468ef08c8b05b54d55cdacdd03acd76c740c682c1fd9df6cfc9`  
		Last Modified: Thu, 17 Aug 2023 22:45:07 GMT  
		Size: 37.0 MB (37028913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5238ddc47a1f8811711e9ec9ff64d761bd88f746ce1e67b6a828cb61c4a9ee39`  
		Last Modified: Thu, 17 Aug 2023 22:44:44 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dab429fda0d374a882dad9b1126903b71148cbb5beaa2e60651cdbd66f90d8`  
		Last Modified: Thu, 17 Aug 2023 22:44:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b196eae5d9b1141759759fa1eedfb26678bcb3fd2bc3f5e9830fd33872a15d7`  
		Last Modified: Thu, 17 Aug 2023 22:44:44 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fdd5e5e69d98c112953f062f0969116bfd175de60931a4f1bb41eed0cf9b10`  
		Last Modified: Thu, 17 Aug 2023 22:44:44 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647dc9812002f22bd02b35f7cff21febc013cb2a182dc0fe43179abb838c3230`  
		Last Modified: Thu, 17 Aug 2023 22:44:44 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee5578f5e36198d9207d97816dad9043cd9933b2c3b85757704098f830c92a`  
		Last Modified: Thu, 17 Aug 2023 22:45:46 GMT  
		Size: 11.4 MB (11409947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:50cf04b2c28272f6a2cadac52bb2f9310e42b0ff0fd1014ef19ba1c6eddacdf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87188239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43cf3e40f59a7d2db3d4589573f6aa0c24ada894a9fee53fbe8ebbc1377d680`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:33 GMT
ADD file:9578bf6d6b33f2ba960ab9309642d1c9dcc131d7b9e6f818b8cc4b843fe3aec8 in / 
# Wed, 16 Aug 2023 01:09:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:02:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Aug 2023 05:02:17 GMT
ENV NGINX_VERSION=1.25.2
# Wed, 16 Aug 2023 05:02:17 GMT
ENV NJS_VERSION=0.8.0
# Wed, 16 Aug 2023 05:02:18 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Aug 2023 05:10:58 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 16 Aug 2023 05:11:00 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 16 Aug 2023 05:11:00 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 05:11:01 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 05:11:01 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 05:11:01 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 16 Aug 2023 05:11:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 05:11:02 GMT
EXPOSE 80
# Wed, 16 Aug 2023 05:11:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Aug 2023 05:11:05 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 16 Aug 2023 05:13:36 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:0500920b409f06d69819525676ebf090702285435050f7b1f973c8c7b034ea7c`  
		Last Modified: Wed, 16 Aug 2023 01:15:59 GMT  
		Size: 33.1 MB (33119300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5e4734fb85966bc8b22f4eb33de6b229d880a99ab63ea8fd64747d645cd14c`  
		Last Modified: Wed, 16 Aug 2023 05:24:54 GMT  
		Size: 41.7 MB (41744699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd71db9cf5a1ef06c0e0ffc5630442e28d20f7bf11a6dfdcc4c93baaf707f64`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80b4b54d9b855bc36c2162921310d2026c63309c0570b8a82ec4d2ce9808ac5`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c54462341e3d92822392d52af0b37090be11c67fef87b1d1fc5912dfb199cd`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb99012aa82b786d1edce7e2cf9bcf5eaf3d799fa6f6d1639a7611ac83ccbc4b`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b88660985b5746617d765b38df878c93f20c4cc45a086dabd2795d15cbfcdb4`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea20de6475d169e73d1aeec063d5d3343427925fb79758d792247f717497a5e`  
		Last Modified: Wed, 16 Aug 2023 05:25:37 GMT  
		Size: 12.3 MB (12319661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-bookworm-perl` - linux; s390x

```console
$ docker pull nginx@sha256:e13218a363924b155f39ada30e6cdb37d02910aa3d0cda6952571651abd05bc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77187417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df76988f804a819a59e3a1968f53708a9bd193023fa83c67720d99a0c9c21e52`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 07 Sep 2023 00:43:39 GMT
ADD file:2a617cce71dc34ce7b62d4b1da4b45cca574c219300ba2be25396630f80bb9cd in / 
# Thu, 07 Sep 2023 00:43:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:08:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 07 Sep 2023 06:08:25 GMT
ENV NGINX_VERSION=1.25.2
# Thu, 07 Sep 2023 06:08:25 GMT
ENV NJS_VERSION=0.8.0
# Thu, 07 Sep 2023 06:08:25 GMT
ENV PKG_RELEASE=1~bookworm
# Thu, 07 Sep 2023 06:11:29 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 07 Sep 2023 06:11:31 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Thu, 07 Sep 2023 06:11:31 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:11:31 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:11:31 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:11:31 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Thu, 07 Sep 2023 06:11:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:11:31 GMT
EXPOSE 80
# Thu, 07 Sep 2023 06:11:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 Sep 2023 06:11:32 GMT
CMD ["nginx" "-g" "daemon off;"]
# Thu, 07 Sep 2023 06:12:23 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
```

-	Layers:
	-	`sha256:68043338ec5d8515f0dcc40f82eb11d30dd8539a1d30984e4b157df8779f6d53`  
		Last Modified: Thu, 07 Sep 2023 00:49:40 GMT  
		Size: 27.5 MB (27489648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df17be13e94ab1d0a793118f67c54831141f5bb04f2675c9b57ea9822e78a79f`  
		Last Modified: Thu, 07 Sep 2023 06:17:29 GMT  
		Size: 37.3 MB (37300565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc1f19898a2ddfdcf87f0d9cec7bacb24531da57f61d13e3fcedf647a7a7e4e`  
		Last Modified: Thu, 07 Sep 2023 06:17:24 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86008c7a20d415648dca1a9293ceeec3730b9f5d7143528f2f0bee40f1dc6f5d`  
		Last Modified: Thu, 07 Sep 2023 06:17:24 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7314bcb915a30e6c6f0a067b3fb999162385357eea131d0d14e2add73d6306`  
		Last Modified: Thu, 07 Sep 2023 06:17:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7451c0c8019aefae2e32421bf0618ea52c48831c88e754483b5b76e94e50d61`  
		Last Modified: Thu, 07 Sep 2023 06:17:24 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b062b3b600b41d5a09430c95b53fd124851f23eebeb9f64ff9a6ff2321515cb`  
		Last Modified: Thu, 07 Sep 2023 06:17:24 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f20203916618362f1c79781b96f1c1d508d999908d5d4fdb41625db85f4f6db`  
		Last Modified: Thu, 07 Sep 2023 06:17:47 GMT  
		Size: 12.4 MB (12392628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
