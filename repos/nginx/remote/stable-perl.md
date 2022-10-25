## `nginx:stable-perl`

```console
$ docker pull nginx@sha256:de58e4c1034ef7e98f34878975b51684e91e0d42e27dd9e5c193b7f935b8a95e
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

### `nginx:stable-perl` - linux; amd64

```console
$ docker pull nginx@sha256:db02ba4f17ead44bb29f45a003aaf7b035cdd19e204e169a80893554e041532e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67988611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9f7bd0523a56249b926455784ce3d3985806c175513fb580784f569aeb55a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:44:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 18:21:11 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 18:21:11 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 18:21:11 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 18:21:54 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 18:21:55 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 18:21:55 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:21:55 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:21:55 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:21:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 18:21:55 GMT
EXPOSE 80
# Wed, 19 Oct 2022 18:21:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 18:21:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ba20091effad485215bb29a8edb43a080817ef80ffa8c798fceb72fabeddcd`  
		Last Modified: Wed, 19 Oct 2022 18:24:39 GMT  
		Size: 36.6 MB (36564748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70dd86f3133e43b9b352045515d20750ec34246f3152d8992d91a36d2d7e11f`  
		Last Modified: Wed, 19 Oct 2022 18:24:33 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c0f2239be648e90be5eadecc697abd555a08f63000edd6fde3474ab16170b`  
		Last Modified: Wed, 19 Oct 2022 18:24:33 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63a9545eccafdff989d1cd08612b9db984868e136499b948f7257251d75002`  
		Last Modified: Wed, 19 Oct 2022 18:24:33 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a724fd887ca6846123b1191e06b6c7b62a3b30ad33e4cd4279f5e9764d399c0`  
		Last Modified: Wed, 19 Oct 2022 18:24:33 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:78aa99fb1667415b5811ccfde79eca1039b629b9e7713f9c58a127ad0f51c895
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63893730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0ded29f04113bd65809f5f59cc13d1a700a704fd53d15192485004ef7ce415`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:34:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 25 Oct 2022 06:43:14 GMT
ENV NGINX_VERSION=1.22.1
# Tue, 25 Oct 2022 06:43:14 GMT
ENV NJS_VERSION=0.7.7
# Tue, 25 Oct 2022 06:43:14 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 25 Oct 2022 06:51:11 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 25 Oct 2022 06:51:11 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Tue, 25 Oct 2022 06:51:12 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Tue, 25 Oct 2022 06:51:12 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Tue, 25 Oct 2022 06:51:12 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Tue, 25 Oct 2022 06:51:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:51:12 GMT
EXPOSE 80
# Tue, 25 Oct 2022 06:51:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Oct 2022 06:51:12 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4e8bfceb96fad857f6aa29d1131279da7078b8e5304624389cad35d058aaef`  
		Last Modified: Tue, 25 Oct 2022 06:53:31 GMT  
		Size: 35.0 MB (34971455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c100e42fba05f4ccadf46c35c2dddcfe6bda5689adecf6b7100a6da373ac011`  
		Last Modified: Tue, 25 Oct 2022 06:53:24 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3f0a600b116232819c1c43f23b413d6724d409fd401e091b76c5587f429ab6`  
		Last Modified: Tue, 25 Oct 2022 06:53:24 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272a25dd613c35bdb5a8e631c1266aa7142c9e5d409ebf50e91314998ffff02`  
		Last Modified: Tue, 25 Oct 2022 06:53:24 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e183507a9e27cc04cfada00f2a8460c1bce44e46fc839f5d127bc96a901c65`  
		Last Modified: Tue, 25 Oct 2022 06:53:24 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:a7634f06a48773bbcef5fb00a5c60e355679fe9f6a9986a0ec9854f297cadf18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60512527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaa096ac0606aeee3de1ba7d3e522a244846ad8d4d331f693b32edc3ae14cfa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 08:14:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 18:23:28 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 18:23:28 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 18:23:28 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 18:32:03 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 18:32:03 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 18:32:03 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:32:03 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:32:04 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 18:32:04 GMT
EXPOSE 80
# Wed, 19 Oct 2022 18:32:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 18:32:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3364cc3858649b08d21495b4aef78c03ae5637c3015045e4fcc7b5b9cd07d`  
		Last Modified: Wed, 19 Oct 2022 18:43:21 GMT  
		Size: 33.9 MB (33929564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38450e2b3e381b3b6edec0ed2b783fc184afc710295a9146edf1da7c2eeeab24`  
		Last Modified: Wed, 19 Oct 2022 18:43:15 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f693230bed90f54a21ce3841173abbcd20fd4f4ea39479ba59f329ecd3dad72`  
		Last Modified: Wed, 19 Oct 2022 18:43:15 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57d57f93392cb6a559ada6b7999ac0a3e47dac1ec26296704efe26c4728801c`  
		Last Modified: Wed, 19 Oct 2022 18:43:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51dd7e7305602f04b2aa12d26fc5c2e0a6d57136f143a4f7f53af7e610b63df`  
		Last Modified: Wed, 19 Oct 2022 18:43:15 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:e6bfad65f0230af70ab8c294805c24177907f4cb62953de8fc6aefc1cae7e620
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66476636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7c30917d4359b89f32734536f4844aa2a52a46ee926701ec67719c9db1df2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:25:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 17:42:14 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 17:42:15 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 17:42:16 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 17:43:09 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 17:43:10 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 17:43:11 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:43:12 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:43:13 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:43:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 17:43:14 GMT
EXPOSE 80
# Wed, 19 Oct 2022 17:43:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 17:43:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b9491e97b5e61d2dae4190a4c5884f48e026202c51ce6fc66754605213d811`  
		Last Modified: Wed, 19 Oct 2022 17:47:06 GMT  
		Size: 36.4 MB (36408483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3705ea76db7445733fbe27d9009972614d365efb83975edbf51cb6249e90b2bb`  
		Last Modified: Wed, 19 Oct 2022 17:47:01 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7797c53f196023a10eeac5e787b298e0c13cd425ae59ed194d1ae4f02c4d4530`  
		Last Modified: Wed, 19 Oct 2022 17:47:01 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f58214000717884ed6356cb4a15471ce1ff6b820e80ca863f635b29e3b93248`  
		Last Modified: Wed, 19 Oct 2022 17:47:01 GMT  
		Size: 771.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf49c2b5d5b7fc53f61bb9257fc04f60b456ad025edc883de3a20d536554459`  
		Last Modified: Wed, 19 Oct 2022 17:47:01 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; 386

```console
$ docker pull nginx@sha256:184a29b8f26560d3bc00e60e07ba4b4f2c4d5358a43704acf36064661b9052a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69375894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2904d7d26ae81710e3a27f207cf197bae8898d6e311a5aaabde9a55749ad878c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:18:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 17:53:00 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 17:53:01 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 17:53:02 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 17:59:47 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 17:59:48 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 17:59:49 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:59:50 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:59:51 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:59:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 17:59:52 GMT
EXPOSE 80
# Wed, 19 Oct 2022 17:59:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 17:59:54 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c31600637f69a4dacef4668509e5f94153f0b252cec046f484aa467241daeda`  
		Last Modified: Wed, 19 Oct 2022 18:09:59 GMT  
		Size: 37.0 MB (36975844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7aeb56dfd04a49f3d62d7aed782fa53b7b42a690a597d7b503f4760bfdfaa1`  
		Last Modified: Wed, 19 Oct 2022 18:09:54 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d649b7fb53a59d8c18d77c516a5016edc70ceec194e43c3613e1e41a486d29a2`  
		Last Modified: Wed, 19 Oct 2022 18:09:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625558bfdfa313aa4ca1ccba72dcd6ae34ed93c57acbddefbcfddcdcf942ca86`  
		Last Modified: Wed, 19 Oct 2022 18:09:54 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841d878455db554598444627487940ce1d2b9f103d0da02df219dcff37afea61`  
		Last Modified: Wed, 19 Oct 2022 18:09:54 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:df052fc5a6824dc41e3b5b8566ef2ff4c2b17a8bfab2af5f56a6e1f28f025bd2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65378957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4ad4730c155a775fecd60f660d993a6a441e93a01a96b4989354bc7229b5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:55:41 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 18:39:30 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 18:39:32 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 18:39:34 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 19:11:03 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 19:11:06 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 19:11:08 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 19:11:10 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 19:11:13 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 19:11:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 19:11:18 GMT
EXPOSE 80
# Wed, 19 Oct 2022 19:11:21 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 19:11:23 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b51d31ee0206acaf82d110d52c3b052814d8eca96f77a7dc72c081e604cdedd`  
		Last Modified: Wed, 19 Oct 2022 19:15:02 GMT  
		Size: 35.7 MB (35734342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbadb25b9248e9ba98af905dc14194a093f941bfc71a11f3fb42512aa7f515f`  
		Last Modified: Wed, 19 Oct 2022 19:14:38 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a1af5691a6878a460fe11f00d91ef8225cffee106094061f14d3a4baf810ba`  
		Last Modified: Wed, 19 Oct 2022 19:14:38 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df334680b96c866788cd172b82303eb78cfc846a707133729de569e179389f`  
		Last Modified: Wed, 19 Oct 2022 19:14:37 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ec3ac70535b0619b19e313aa214872b2fb8a106c73ed158e00e5b1bb5ab040`  
		Last Modified: Wed, 19 Oct 2022 19:14:38 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:25a87157239dd855db0a9c64dfa9c6120e0b72c99b5c0c9bcbb1277631b35fb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d663b069c8f294eefbb530e987a267ca3897c6a2fa25ba05a3bcd335e906e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:40:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Aug 2022 02:47:38 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 23 Aug 2022 02:47:38 GMT
ENV NJS_VERSION=0.7.6
# Tue, 23 Aug 2022 02:47:38 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 23 Aug 2022 02:56:06 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 23 Aug 2022 02:56:08 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 23 Aug 2022 02:56:09 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 23 Aug 2022 02:56:09 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 02:56:10 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 02:56:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:56:10 GMT
EXPOSE 80
# Tue, 23 Aug 2022 02:56:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Aug 2022 02:56:11 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7462398c107e9fe7a5d78b7b8316f383e990eab29d4f3ff19f7f29c95b774a92`  
		Last Modified: Tue, 23 Aug 2022 02:58:15 GMT  
		Size: 38.6 MB (38603804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa1a9ba0a4116334d537b908ba3178027b55b2d0790d27f0579fcec8537c97b`  
		Last Modified: Tue, 23 Aug 2022 02:58:05 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea9277a99d2f6a532410b8208d25bc36b1bab4208e1580b9c894f009b04a37a`  
		Last Modified: Tue, 23 Aug 2022 02:58:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ddabe49378537582958879e8083dad0428297d3aba57847ceb4447d43c1ed6`  
		Last Modified: Tue, 23 Aug 2022 02:58:05 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e66bc0a79e363e80a29b9c4a866047da0723cf90e5df82fbf29c6b8664adac8`  
		Last Modified: Tue, 23 Aug 2022 02:58:05 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; s390x

```console
$ docker pull nginx@sha256:65efa878312031718f927ff0c517f3c02dce15b4d8813680bcf27d768c553b4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66331615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416d252c70cfe4815ab4292141805cf76b37762c9d43364f96f1b347e45a21cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:27:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Oct 2022 01:31:12 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 05 Oct 2022 01:31:13 GMT
ENV NJS_VERSION=0.7.6
# Wed, 05 Oct 2022 01:31:13 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 05 Oct 2022 01:34:52 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 05 Oct 2022 01:34:54 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 05 Oct 2022 01:34:54 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 05 Oct 2022 01:34:54 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 05 Oct 2022 01:34:54 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 05 Oct 2022 01:34:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:34:54 GMT
EXPOSE 80
# Wed, 05 Oct 2022 01:34:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 01:34:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5fab1e1ab59a55484c9091cf432e7c38613a53142ad5438b34f15315493850`  
		Last Modified: Wed, 05 Oct 2022 01:36:36 GMT  
		Size: 36.7 MB (36677342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353d60a40721dd27c46bf29965d1d146ccca17dfe11faee2bdc14030814e3c95`  
		Last Modified: Wed, 05 Oct 2022 01:36:31 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b016d14818a12bcdf4ac503fd0da13728a122f1a40e334cc4384d33c7c5a3939`  
		Last Modified: Wed, 05 Oct 2022 01:36:31 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0974ef004080088ff358052356154d8ea0827a8a09dc6e3149b69170727db2`  
		Last Modified: Wed, 05 Oct 2022 01:36:31 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a818912f97a6dc162566847de1460db6fa3431913c0773b00fb618674cd2feb1`  
		Last Modified: Wed, 05 Oct 2022 01:36:31 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
