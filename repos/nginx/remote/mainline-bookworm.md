## `nginx:mainline-bookworm`

```console
$ docker pull nginx@sha256:543478db8f63da81aab4989cbab0cd2086b50dba97954e8e50c1cf77f020a2e5
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

### `nginx:mainline-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:48a84a0728cab8ac558f48796f901f6d31d287101bc8b317683678125e0d2d35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70467699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea7b3dcba7ee47c0d16a60cc85d2b977d166be3960541991f3e6294d795ed24`
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

### `nginx:mainline-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:564758eea033ca83d7b79f8b9100fc8f7ace7937de905f2afba5c4950d768cd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63158408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bce0ef01dcf257c44638498cffb3335ce7415eee1555bed96d714d930a2f78a`
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

### `nginx:mainline-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ab01fca45d6c3ceb8d7b72364eb03a8b47377b5d42cf1433dcf28d365544f1d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59513498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d6ae7af1a42044afa3618e40bb26feedf9839c1baa244805f3195c8c765aba`
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

### `nginx:mainline-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:85eabf2757cb5b5b84248d7feb019079501dfd8691fc79b8b1d0ff1591a6270b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67178407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91582cfffc2d0daa6f42adb6fb74665a047310f76a28e9ed5b0185a2d0f362a6`
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

### `nginx:mainline-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:5cb875708d73e81a17536bb72e60d151ca9288e183dacf3796a1bea956546b11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68626900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d3876faad88cb363adb765c65a35a3412f0d14fb451b29d53988380e90645d`
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

### `nginx:mainline-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:12955060f28a99591888e74bea46171b8bee67869c3cf9e47dbb557feba288ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66154974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d100bc7f218656407fb7f65c2be5065887b958b7cbd405f3a79ff7c42ecb3a`
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

### `nginx:mainline-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:3060cd691cdf5e1a1cf1dfcc0354bbba647808f1dfb530f51d934b2ee766f385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74868578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c713f97f940032933b50f6b0271e93e5db584d15d1777226637c49a51fdf06`
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

### `nginx:mainline-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:968ca27471c39e881787859f77ca757690f2c81bfe87c83384853e2d4f8861a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64794789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90eb2db2e1759f7fa7b90cb5d466691ed9835b69e04e395251e0fa67b660b95`
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
