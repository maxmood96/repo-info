## `nginx:stable-perl`

```console
$ docker pull nginx@sha256:d0aa95b1bfa9c05ced02d6ec996c302a8169ada79a5df04174ed05a0e2951abf
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
$ docker pull nginx@sha256:1cfac6bf8a435d23049021ce3e76da683a3d1c43fe55050bb34eb38748a78bad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64676199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7b0be24eed476c991874394fa387ee984c526f68268763e2875505399371ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:03:10 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 02:04:21 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 02:04:21 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 02:04:21 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 02:05:14 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:05:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 02:05:16 GMT
EXPOSE 80
# Tue, 12 Oct 2021 02:05:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 02:05:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed628001eed34161794c452a02805ab3845ee492a62ea3c581aeaa3eae1af685`  
		Last Modified: Tue, 12 Oct 2021 02:07:11 GMT  
		Size: 37.5 MB (37533142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817211fec02631968ec81762ea1349c1e90ce92f0b95ffa759964bc7b3000ad0`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f2099533cd2e254e6975d94959710c3285f8d573a443e66f634b27d4263b33`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3f41dff7d220fb9c1d47d21eb6079626b11f1addc52782d0144f96022af104`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9097ac386706e3c49e62b0dc72e626ba4bcbab2c1894b7b75158baf315cdc81b`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:9ef3f1d3bbbba76a0b154f4931f6f8fe17d95415c656d57cb9d65d42815e61ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60597738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc193872f07b68f14eefa63c2ea053137cff05b17f3ea7c6b86d6cb19b3b9113`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 00:51:32 GMT
ADD file:0d95eee31ffe3f4260263e4fac2a61123a4b98d2e7a67efcc7bfea338c54f41d in / 
# Tue, 12 Oct 2021 00:51:32 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:31:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 16:50:53 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 16:50:54 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 16:50:54 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 17:09:56 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 17:09:57 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 17:09:57 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 17:09:58 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 17:09:58 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 17:09:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 17:09:59 GMT
EXPOSE 80
# Tue, 12 Oct 2021 17:10:00 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 17:10:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:175b083b22fb061f7d1894fe4916a2967ce636d47376da526d90d57c8f7efc60`  
		Last Modified: Tue, 12 Oct 2021 01:07:45 GMT  
		Size: 24.9 MB (24872704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0109ba2d8adbba667a4c4be7aca5303f77beddbb13986726af1081cf36c5f9`  
		Last Modified: Tue, 12 Oct 2021 17:13:54 GMT  
		Size: 35.7 MB (35721468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00471979cbcf8b0a0baf72c8c4cc77d31828b97bcda503c818e4adf21bc3932f`  
		Last Modified: Tue, 12 Oct 2021 17:13:29 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c688c677e520668552abd0a97421f6cb392fef0f41c0d40f265a52da31b470`  
		Last Modified: Tue, 12 Oct 2021 17:13:29 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebd7aa3bcfbf696ad3ebb837a28d0891845c7f0e3c6d4ab4f6af3168dcfd2bb`  
		Last Modified: Tue, 12 Oct 2021 17:13:29 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9320054dacbbab2f5337e071d4bf20529a0235caf6f9fbe0fd8c0cfc784c67c1`  
		Last Modified: Tue, 12 Oct 2021 17:13:29 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ee2b1f56cd65e6407716b7573ad3d032114ac6834028e4033765db290bc69aac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57354904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a9eaa92842ba084da5863c3c2dbe14edd60c0e234a6c316ffba96e3b1eac7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:10:41 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 06:29:29 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 06:29:29 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 06:29:30 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 06:47:01 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 06:47:02 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 06:47:03 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 06:47:04 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 06:47:04 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 06:47:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 06:47:05 GMT
EXPOSE 80
# Tue, 12 Oct 2021 06:47:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 06:47:06 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cdb8168892949fde35cc30a5b84ac896304c629d76c346da17475a9f1c598e`  
		Last Modified: Tue, 12 Oct 2021 06:52:24 GMT  
		Size: 34.6 MB (34611648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40383a8b5b629a437f7ca1fc45bdec63fb6a55c66cba5397ba118ac4ac0b8`  
		Last Modified: Tue, 12 Oct 2021 06:52:05 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9be0d1a57f4aa4c1d30c4a90f690ae49a00c5aa3687037b219a533a70a95b2a`  
		Last Modified: Tue, 12 Oct 2021 06:52:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7894f34350596ff99c55893b46683249fc763beced4a5cf2af7e46aae28c6b3e`  
		Last Modified: Tue, 12 Oct 2021 06:52:05 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea035d225970886657569827a4b8caf4813a6a24a00cccbdfa9d3cebd04fe53`  
		Last Modified: Tue, 12 Oct 2021 06:52:05 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a80e2b520acf66a40532d13d089a1325360102d8919bdd533bec07b2a3121800
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63165388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa0322bc6fc0363415b461095a507d5e0c6a9a7eaf285fd916ea65d476b9f1d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:42 GMT
ADD file:f0d53027a7ba594477674127971aa477af3a2bc6bcddef6c0aa174953a5f2db0 in / 
# Tue, 12 Oct 2021 01:41:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:36:40 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 04:37:57 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 04:37:57 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 04:37:58 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 04:38:49 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 04:38:49 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 04:38:49 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 04:38:49 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 04:38:50 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 04:38:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:38:50 GMT
EXPOSE 80
# Tue, 12 Oct 2021 04:38:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 04:38:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:02b45931a436a68cadb742684148ed6aacbbf9aa21447b467c11bac97f92eb46`  
		Last Modified: Tue, 12 Oct 2021 01:49:07 GMT  
		Size: 25.9 MB (25908479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cb0748f35fe7e4b350ad1bdab4399fdc6fb9786e39bf55fab4177433769a35`  
		Last Modified: Tue, 12 Oct 2021 04:41:34 GMT  
		Size: 37.3 MB (37253361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92741845059b0fdbe60717f08119d8ead344c91fd7459c100d0d46505fb2be5b`  
		Last Modified: Tue, 12 Oct 2021 04:41:28 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1570b905943d0cf6f14ce3f7d9bed6e643197da3992a265532c3743f284e3`  
		Last Modified: Tue, 12 Oct 2021 04:41:28 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1f959554fda4c562a04796313fe1272f833599dd730791b5d8c88f9554e586`  
		Last Modified: Tue, 12 Oct 2021 04:41:28 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1f4d66dc5e1d8c3c34b899de89177e98a04eda90ba8bead74b65412e35411d`  
		Last Modified: Tue, 12 Oct 2021 04:41:28 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; 386

```console
$ docker pull nginx@sha256:62e69b2611c8abe895fe920657c48de2df2f0f5b286b21f7c3dbdafc9ccce404
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65649937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd95e06229b9057ec034823fe2d9efba97a0aeab06f7acf5e033af52ed561ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 01:40:17 GMT
ADD file:1b432d2306b487c59442b30c65ddabd08b45484c6ce09b0c25112c29f4a98f17 in / 
# Tue, 12 Oct 2021 01:40:17 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:36:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 02:38:57 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 02:38:57 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 02:38:57 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 02:40:02 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 02:40:02 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 02:40:02 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:40:03 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:40:03 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 02:40:04 GMT
EXPOSE 80
# Tue, 12 Oct 2021 02:40:04 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 02:40:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:860d012fe46ce39c3737ace24d10d8ad65ae9c78abde6891ca6e97b0d7f271dd`  
		Last Modified: Tue, 12 Oct 2021 01:48:37 GMT  
		Size: 27.8 MB (27791445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d7d9a85602841f979c41de7cd17f7521f342dec0a8eaa76bd6a09c316cc462`  
		Last Modified: Tue, 12 Oct 2021 02:42:39 GMT  
		Size: 37.9 MB (37854936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c395ca9a1c75ce42744cd4ff661e7f6ac792b30b92774eb474ea32b2ecd81b`  
		Last Modified: Tue, 12 Oct 2021 02:42:30 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bd55e634a2f67fdb69d5f4f553d60c1dd70cdc93e2180d24955a2b7cab40a8`  
		Last Modified: Tue, 12 Oct 2021 02:42:30 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2c0353f4c86feb84d40894256ddb4608199f0ff9a62b29167ee9a52aebd431`  
		Last Modified: Tue, 12 Oct 2021 02:42:30 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a345636719953db53b185e1b9c8898ac3d54f7ce843a5d57107578ec0f1e16c`  
		Last Modified: Tue, 12 Oct 2021 02:42:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:25c44a2d5f1813a3d95a7614b8fc4569fe42fd85404fd4d5ded765e1cee3f35a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62169273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdb558d8db1b76ac84f3e55b0768bbab63b5a8ba854851f173527385167c8da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 03 Sep 2021 01:10:49 GMT
ADD file:219b2ce847fd4b227257f60cf40dee2eaf7688371fd76658752f6ccbac9c4353 in / 
# Fri, 03 Sep 2021 01:10:49 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:40:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 Sep 2021 03:05:18 GMT
ENV NGINX_VERSION=1.20.1
# Fri, 03 Sep 2021 03:05:19 GMT
ENV NJS_VERSION=0.5.3
# Fri, 03 Sep 2021 03:05:19 GMT
ENV PKG_RELEASE=1~buster
# Fri, 03 Sep 2021 03:29:38 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 03 Sep 2021 03:29:39 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 03 Sep 2021 03:29:40 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 03 Sep 2021 03:29:40 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 03 Sep 2021 03:29:41 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Fri, 03 Sep 2021 03:29:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 Sep 2021 03:29:41 GMT
EXPOSE 80
# Fri, 03 Sep 2021 03:29:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 Sep 2021 03:29:42 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c11f388d181c313e7657eea7b1ffa2d20856b4701922412adea724a19acdb79f`  
		Last Modified: Fri, 03 Sep 2021 01:19:51 GMT  
		Size: 25.8 MB (25812853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3cfaeea6251141a520dac0649b0c1f72b5c7aee78036ac1ab155b60a7dcc7`  
		Last Modified: Fri, 03 Sep 2021 03:32:18 GMT  
		Size: 36.4 MB (36352857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebeceabf601bfd61da8b23d377b6153f6939860ed7a537062f6b08c7d8a3406e`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dcd22174cf8c8aca6ef6e9d174e7e2f7b72f8d9541c69209e1ace5385abed1`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d2a2ea78058d58f9873cbdaa26206599cabad4c425f34a4e65090ae5e0afa8`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde816196961dbb389e2ed9932c2eb6a5a6742068ec1d51799f4211826936074`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:bdd1189016c17bcf2987e2b4ad9ec355ccc68cfb8a62ad9215ca023f60e42df4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70389224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a21b33e401ed52dd1a12c21de79f0246b6ae9d7689e3332701f586f7f7fd575`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:45:43 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 08:28:54 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 08:29:00 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 08:29:09 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 09:13:17 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 09:13:23 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 09:13:27 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 09:13:31 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 09:13:34 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 09:13:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 09:13:46 GMT
EXPOSE 80
# Tue, 12 Oct 2021 09:13:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 09:13:52 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfaca55618471c5f12694852b4fdd91ef415a01a74bea207ee6378969f5d00c`  
		Last Modified: Tue, 12 Oct 2021 09:16:59 GMT  
		Size: 39.8 MB (39838463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9448ede38bbe2a11129fb2a9d06fd2a9c823bfede14c6d047337bbdea5018ff0`  
		Last Modified: Tue, 12 Oct 2021 09:16:51 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6266c9028f4bd8b142b33d9173a5a31f14a64b5212e60ae6f36469e4879bd`  
		Last Modified: Tue, 12 Oct 2021 09:16:51 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73ca18ad5940285dcc0761fb08814884dec854c1539805ab26f92ab0b3191e8`  
		Last Modified: Tue, 12 Oct 2021 09:16:51 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e673f0c263fd64719a564979d8ebf6e668e13390634aacb344a32bf2dd688a`  
		Last Modified: Tue, 12 Oct 2021 09:16:51 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; s390x

```console
$ docker pull nginx@sha256:414ebc2499cf9228f014f3e958d7b6054ec737894466baa1280c8911c092d385
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63144475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a701973c97024c4611a3ad90a3fd305f86053f306e35ff608973c1e9867e73dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:56 GMT
ADD file:39da9acd4d06d69f3ca8d25ef5c097ae741972d6b15a6a057bc7487380157b61 in / 
# Tue, 12 Oct 2021 00:42:57 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:58:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 07:04:38 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 07:04:38 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 07:04:38 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 07:09:44 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 07:09:46 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 07:09:46 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 07:09:46 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 07:09:46 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 07:09:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 07:09:47 GMT
EXPOSE 80
# Tue, 12 Oct 2021 07:09:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 07:09:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:78a640c6bb4733e5156ce97c5ec773cf97b357c3a07244348384da5060788a61`  
		Last Modified: Tue, 12 Oct 2021 00:48:41 GMT  
		Size: 25.8 MB (25754252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d492abe775ddb43cb9433b060abbe81fbc55de3ad003aab1aad9a2cd4b8fc91`  
		Last Modified: Tue, 12 Oct 2021 07:12:13 GMT  
		Size: 37.4 MB (37386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbdb2ded7afde13a79748dea44872ec7e762c792d8de522bef6163a51c063a0`  
		Last Modified: Tue, 12 Oct 2021 07:12:03 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98af02ef3569f5aad8df2c0e3ac4b07f5d98c4b23225c4986211388de0ce1360`  
		Last Modified: Tue, 12 Oct 2021 07:12:03 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362bf7c6a3923a81562965ee020442c2f12ab216c2cd822364f8a11c9dc96028`  
		Last Modified: Tue, 12 Oct 2021 07:12:03 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb938982eb41b38f4b321d73dc4a9d30ea2e9892867f978a2239b1b205937292`  
		Last Modified: Tue, 12 Oct 2021 07:12:03 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
