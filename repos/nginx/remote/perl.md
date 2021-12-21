## `nginx:perl`

```console
$ docker pull nginx@sha256:1428a63678d038f32b7f588033b805e4869b1bfe2f3fdbae1da615143b073d31
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

### `nginx:perl` - linux; amd64

```console
$ docker pull nginx@sha256:9a0b1c7ce51928b00d0eadc92c97cfda713ff84366617662d8e11b7aced9ab69
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67883469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481375b6e9f29c0c00e155057fb6474024b4a094b72081b528a50a49c152e618`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:00:06 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 21 Dec 2021 03:00:06 GMT
ENV NGINX_VERSION=1.21.4
# Tue, 21 Dec 2021 03:00:06 GMT
ENV NJS_VERSION=0.7.0
# Tue, 21 Dec 2021 03:00:06 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 21 Dec 2021 03:01:15 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 21 Dec 2021 03:01:16 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 21 Dec 2021 03:01:16 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 21 Dec 2021 03:01:16 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 03:01:17 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 03:01:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 03:01:17 GMT
EXPOSE 80
# Tue, 21 Dec 2021 03:01:18 GMT
STOPSIGNAL SIGQUIT
# Tue, 21 Dec 2021 03:01:18 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277eafb9423cfd1d92346b898971c6cae39d85332579208445672ec7ad425b76`  
		Last Modified: Tue, 21 Dec 2021 03:04:02 GMT  
		Size: 36.5 MB (36522286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008b20d174ec2f7da620eec6b095e3dbdd66a4d311ff76c8964d1cc023bdd237`  
		Last Modified: Tue, 21 Dec 2021 03:03:55 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cf1ff9306d5f74c853f5a445452c6b466fc1d4907141e7b37eadc24a120464`  
		Last Modified: Tue, 21 Dec 2021 03:03:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccdb94cdbd99605022afb4d6b0262aa1ba16828b15bc6f17b76fb383d72bfee`  
		Last Modified: Tue, 21 Dec 2021 03:03:55 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35e54404fc7e181d31dc2bc56995d7b6f53f096d6d8b0d12879da9d53203a8a`  
		Last Modified: Tue, 21 Dec 2021 03:03:55 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:892cb96cfe207db7bd1845507f61adc010f3c2ac0b5948a96190b5087b2564c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63849799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c6f3cac0faabd2478296f90622779702ec38e0ec423776c9b73cca7e3fb57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:37 GMT
ADD file:7debbdb237139cb08189976f79cfa64cfd71f5cc98dfb2f560b558acb5f7cec9 in / 
# Thu, 02 Dec 2021 02:50:38 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 05:14:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 02 Dec 2021 05:14:58 GMT
ENV NGINX_VERSION=1.21.4
# Thu, 02 Dec 2021 05:14:59 GMT
ENV NJS_VERSION=0.7.0
# Thu, 02 Dec 2021 05:15:00 GMT
ENV PKG_RELEASE=1~bullseye
# Thu, 02 Dec 2021 05:40:54 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 02 Dec 2021 05:40:55 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Thu, 02 Dec 2021 05:40:56 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Thu, 02 Dec 2021 05:40:57 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 02 Dec 2021 05:40:57 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Thu, 02 Dec 2021 05:40:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 05:40:58 GMT
EXPOSE 80
# Thu, 02 Dec 2021 05:40:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Dec 2021 05:40:59 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c5e429166894878430c39748965935f89ffa957667340c3c8bd872418dbce663`  
		Last Modified: Thu, 02 Dec 2021 03:09:28 GMT  
		Size: 28.9 MB (28910824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066365564066b4a9420bedf3553f72be42d93658897c87397d8884029d6ef3e`  
		Last Modified: Thu, 02 Dec 2021 05:50:59 GMT  
		Size: 34.9 MB (34935414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8206fd1d06bcd93437fad2ac981ca9eb890eb104befc007e4ceab1280ed0edda`  
		Last Modified: Thu, 02 Dec 2021 05:50:44 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26509b049f4c059bee3e08da3420f449764595a7b7c5d8e7881e055f10aba65`  
		Last Modified: Thu, 02 Dec 2021 05:50:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5f7656678b92d5b1258fb12f9434c76bc2e06b8fa2aac8fd2b917444a8dfb9`  
		Last Modified: Thu, 02 Dec 2021 05:50:44 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0f08f5e9e774947287292ac06f00d8b4b892fd9526e98990f1726761c91c9`  
		Last Modified: Thu, 02 Dec 2021 05:50:44 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:1c74e7f3c7b70b955f19e86ddb2f331980c491b3b5eb2316eb8e2199c91ed6ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60465805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a40cf5a1cc4fdc0dcefcbf43774d7ff268797ac817c90230d0a7a0d780acf52`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:45:52 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 02 Dec 2021 17:45:52 GMT
ENV NGINX_VERSION=1.21.4
# Thu, 02 Dec 2021 17:45:53 GMT
ENV NJS_VERSION=0.7.0
# Thu, 02 Dec 2021 17:45:53 GMT
ENV PKG_RELEASE=1~bullseye
# Thu, 02 Dec 2021 18:04:50 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 02 Dec 2021 18:04:51 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Thu, 02 Dec 2021 18:04:52 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Thu, 02 Dec 2021 18:04:52 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 02 Dec 2021 18:04:53 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Thu, 02 Dec 2021 18:04:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 18:04:54 GMT
EXPOSE 80
# Thu, 02 Dec 2021 18:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Dec 2021 18:04:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8427ad81959710904083a1ccd957cd119204a845871c6fd271ca64af23473b21`  
		Last Modified: Thu, 02 Dec 2021 18:28:01 GMT  
		Size: 33.9 MB (33889055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fc009985396d1a7030d8f4e3feccb969fedb5e08b95aa1de361b02b396b46a`  
		Last Modified: Thu, 02 Dec 2021 18:27:39 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0497c737dca6a14d399d90b6d525069cf42bc927f0807d4230e4880a441dd49e`  
		Last Modified: Thu, 02 Dec 2021 18:27:39 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e0fdd7b8b5c7dfa86892225969e52cc7b56c02c37b34bd5698f7c1604b5731`  
		Last Modified: Thu, 02 Dec 2021 18:27:39 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10c900d0e1c2c3feacab37f655a0bb3de5348623e8619d31c5451e95ed1af5`  
		Last Modified: Thu, 02 Dec 2021 18:27:39 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a1603e9822e15e439e15c017226adfc30834d6bbf09ce6b7762ef65e375577b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66398777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e12d1b70f8b56d0ede8328610a67c22340c7bf6e781de37471109f4692aba2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:46:18 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 21 Dec 2021 02:46:19 GMT
ENV NGINX_VERSION=1.21.4
# Tue, 21 Dec 2021 02:46:20 GMT
ENV NJS_VERSION=0.7.0
# Tue, 21 Dec 2021 02:46:21 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 21 Dec 2021 02:47:26 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 21 Dec 2021 02:47:27 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 21 Dec 2021 02:47:28 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 21 Dec 2021 02:47:29 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 02:47:30 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 02:47:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:47:31 GMT
EXPOSE 80
# Tue, 21 Dec 2021 02:47:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 21 Dec 2021 02:47:33 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930694c324106be6771cba80d4fa3096f7bb102e97ec0867e23ee92c7d045c1`  
		Last Modified: Tue, 21 Dec 2021 02:50:49 GMT  
		Size: 36.4 MB (36351432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a48a0c755e71122ff33d5d6eb694557794942cc17a1497385994ece68a3e197`  
		Last Modified: Tue, 21 Dec 2021 02:50:43 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04dbb0dfd50c2381c8e8e726ac415c24dc5b918b21eca4db13254fc7135c6d3`  
		Last Modified: Tue, 21 Dec 2021 02:50:43 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181357732dce688b35cca5b52ad6e5d95eca9914d14364dc2b8722f7eeb785a`  
		Last Modified: Tue, 21 Dec 2021 02:50:43 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e58c7c4d4d591b58a1ff701223625226f9c6c0aebdebfb87085b8c593e444d`  
		Last Modified: Tue, 21 Dec 2021 02:50:43 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; 386

```console
$ docker pull nginx@sha256:c10c26c5485253b7b7445bb0094bfd2b4819405680a4039bc46aef504cd6a6c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69318383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b393f5bb8c3c2db80d469b519c5ca0fd649053a1e93fbb3a31e19d391219d0d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:34:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 02 Dec 2021 09:34:44 GMT
ENV NGINX_VERSION=1.21.4
# Thu, 02 Dec 2021 09:34:44 GMT
ENV NJS_VERSION=0.7.0
# Thu, 02 Dec 2021 09:34:45 GMT
ENV PKG_RELEASE=1~bullseye
# Thu, 02 Dec 2021 09:45:10 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 02 Dec 2021 09:45:11 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Thu, 02 Dec 2021 09:45:11 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Thu, 02 Dec 2021 09:45:12 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 02 Dec 2021 09:45:12 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Thu, 02 Dec 2021 09:45:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 09:45:13 GMT
EXPOSE 80
# Thu, 02 Dec 2021 09:45:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Dec 2021 09:45:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171f614c8ec18efc4686ce9b40cc1acc5a443ef42e7d38a02f862ae2a988bddf`  
		Last Modified: Thu, 02 Dec 2021 09:57:20 GMT  
		Size: 36.9 MB (36934014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca2b5f333bdf91810b8a5d1d4dae54d6651312c589101d32dda0e63c72eb29`  
		Last Modified: Thu, 02 Dec 2021 09:57:11 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350ca1d138320ef39681154b5375a0e922fc7aed2452948b4b190273b4d7e8a`  
		Last Modified: Thu, 02 Dec 2021 09:57:12 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2573c1d2448fbad3c81ae2b29d6f77b6e65595c7593756b088c79be757ab2746`  
		Last Modified: Thu, 02 Dec 2021 09:57:11 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fde96f6c7437c83e7827a6f15ef910b379de953fe3bea1f8fe0d0507500873`  
		Last Modified: Thu, 02 Dec 2021 09:57:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; mips64le

```console
$ docker pull nginx@sha256:0c0d91ce73199dac7351892323fd01a0e99dae17928db5e03d1ae865ea627658
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65294892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb40d89bb5a957aebe14638ee3ffebb3fe4aef0de46c25cbf073e09ef5d5cea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 04:03:28 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 21 Dec 2021 04:03:28 GMT
ENV NGINX_VERSION=1.21.4
# Tue, 21 Dec 2021 04:03:29 GMT
ENV NJS_VERSION=0.7.0
# Tue, 21 Dec 2021 04:03:29 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 21 Dec 2021 04:31:53 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 21 Dec 2021 04:31:53 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 21 Dec 2021 04:31:54 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 21 Dec 2021 04:31:54 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 04:31:55 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 04:31:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 04:31:55 GMT
EXPOSE 80
# Tue, 21 Dec 2021 04:31:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 21 Dec 2021 04:31:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6b43cb495d18fcf5fd7f42b62c9f72c0a6511f8eab5aacaacd418202adc857`  
		Last Modified: Tue, 21 Dec 2021 05:02:38 GMT  
		Size: 35.7 MB (35672152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e68f245a0e499da906045685b466c8a9c7ebbbd8254e03bd9ba1f2bb3bf19ec`  
		Last Modified: Tue, 21 Dec 2021 05:02:13 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892eadab94245e93ebeed9b9891ae9a1291eb7fd57935814f7b566731e21105`  
		Last Modified: Tue, 21 Dec 2021 05:02:14 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050333170294c2800755d924c2f04fbea1a0afa1d017c368ccc78bc779c6c22c`  
		Last Modified: Tue, 21 Dec 2021 05:02:13 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ffef89602abcafa70b05b25d7eab6622482200b8fb14314cef7cc7ceddaa9`  
		Last Modified: Tue, 21 Dec 2021 05:02:13 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:d01bca8ba4063de8939afb7ac05ce280c37ad4c6dc0a4b7869f8632b304d31dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73828795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94406fda7bc64f43df21edcf8570394b08eadf1c5b071cc9f097c5efb4ea925b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 05:24:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 21 Dec 2021 05:24:26 GMT
ENV NGINX_VERSION=1.21.4
# Tue, 21 Dec 2021 05:24:28 GMT
ENV NJS_VERSION=0.7.0
# Tue, 21 Dec 2021 05:24:29 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 21 Dec 2021 05:42:24 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 21 Dec 2021 05:42:27 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 21 Dec 2021 05:42:28 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 21 Dec 2021 05:42:29 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 05:42:30 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 21 Dec 2021 05:42:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 05:42:32 GMT
EXPOSE 80
# Tue, 21 Dec 2021 05:42:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 21 Dec 2021 05:42:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9fae0a1f9e014edee6d29fa1af736729637f28a260f741dcbd0759f8745c45`  
		Last Modified: Tue, 21 Dec 2021 05:56:48 GMT  
		Size: 38.6 MB (38566240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0243bbda9123dd10ad6398944d79a89b8b753d7d6b63fd324c8f26cbf83c472f`  
		Last Modified: Tue, 21 Dec 2021 05:56:40 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072868326368d978e674486de992c0384c9b3851ab4334b7f4ad730df874d5a`  
		Last Modified: Tue, 21 Dec 2021 05:56:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924afb5a6eae33fcf6fee7dd0fe1c8d76ae54e80a25267cf8a23180480d3c88d`  
		Last Modified: Tue, 21 Dec 2021 05:56:40 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6a78612127d20c34f2de5f27bc2faca6c97bbb6b824b5f84558b24be0b72ac`  
		Last Modified: Tue, 21 Dec 2021 05:56:40 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:perl` - linux; s390x

```console
$ docker pull nginx@sha256:2946ffbae1ac42a9d5be5695edd1184b758722a46c47f2a629f87fddb75a106d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33af7aaf874955848906b25e04c0747867e9a83c355e1ccfde6309ec5e6ef16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:11:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Nov 2021 04:11:12 GMT
ENV NGINX_VERSION=1.21.4
# Wed, 17 Nov 2021 04:11:13 GMT
ENV NJS_VERSION=0.7.0
# Wed, 17 Nov 2021 04:11:13 GMT
ENV PKG_RELEASE=1~bullseye
# Fri, 19 Nov 2021 01:53:30 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 19 Nov 2021 01:53:32 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 19 Nov 2021 01:53:32 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 19 Nov 2021 01:53:32 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 19 Nov 2021 01:53:33 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Fri, 19 Nov 2021 01:53:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Nov 2021 01:53:33 GMT
EXPOSE 80
# Fri, 19 Nov 2021 01:53:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Nov 2021 01:53:33 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d4749453667ebd955e46658f42d8f5d8cef51f4c91c8d5741befc7ea8c718e`  
		Last Modified: Fri, 19 Nov 2021 01:59:07 GMT  
		Size: 36.7 MB (36652587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2385e9e0a25b57a291fa429896f3610c793cf2313203ec989c46c2dcfe5c5456`  
		Last Modified: Fri, 19 Nov 2021 01:59:02 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878b7e5d9b2e8b472c18819a96d9cacd51e9336783cb4ef52d844cbc4f58976`  
		Last Modified: Fri, 19 Nov 2021 01:59:02 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e1c28d06620052da84cf5b6a024e38294a00585e49b48af87338140d71d468`  
		Last Modified: Fri, 19 Nov 2021 01:59:02 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d2d264c0cb3515c36964846f59eee611e0e7d004209fc89e052acd2dca322d`  
		Last Modified: Fri, 19 Nov 2021 01:59:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
