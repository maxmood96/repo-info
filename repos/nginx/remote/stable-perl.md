## `nginx:stable-perl`

```console
$ docker pull nginx@sha256:138f285ba1bdfb3528dc77389bfbcb382d7db848df60c70291a495fc0da84e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
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
$ docker pull nginx@sha256:7054edf51617b7c8e9796a7d05e97ed154709c68a4a33e03016d39271e6ebc0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64514728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9410649c73c0346dabb2c5fcb04d43c4fcc81f693fe7506f17c3e66b1bc4883`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:39:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Oct 2020 08:40:47 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 13 Oct 2020 08:40:47 GMT
ENV NJS_VERSION=0.4.4
# Tue, 13 Oct 2020 08:40:48 GMT
ENV PKG_RELEASE=1~buster
# Tue, 13 Oct 2020 08:41:58 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 13 Oct 2020 08:41:58 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Thu, 05 Nov 2020 18:22:14 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 18:22:14 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 18:22:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Nov 2020 18:22:14 GMT
EXPOSE 80
# Thu, 05 Nov 2020 18:22:15 GMT
STOPSIGNAL SIGTERM
# Thu, 05 Nov 2020 18:22:15 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ac678eee2fae9241ad7856652153659bff905448b1ae5215e467d780902bf0`  
		Last Modified: Tue, 13 Oct 2020 08:43:07 GMT  
		Size: 37.4 MB (37420344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff2196aeccb4dd86fb5386661dab2dc5166f909db9c073277e41f80ee726e84`  
		Last Modified: Tue, 13 Oct 2020 08:42:59 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6374f505d1f63afce4a85df209fc035a6e30bbf653da88ae3f760ec743e2613`  
		Last Modified: Thu, 05 Nov 2020 18:23:38 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dd991288873300f37a4e7645f53d855f3d877dc4d1cd6679c8b95e480ee9cb`  
		Last Modified: Thu, 05 Nov 2020 18:23:38 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:341c58bb2c7ce455d070b8026a0001760b33ebc6464f6b4695416ed6707f95c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60440308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba4701103fcf8ae4e74542020edaab7f450eb67ebad7d7e5f783f18674a5190`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:47:28 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Oct 2020 03:02:52 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 13 Oct 2020 03:02:53 GMT
ENV NJS_VERSION=0.4.4
# Tue, 13 Oct 2020 03:02:55 GMT
ENV PKG_RELEASE=1~buster
# Tue, 13 Oct 2020 03:17:36 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 13 Oct 2020 03:17:44 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Thu, 05 Nov 2020 19:03:36 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 19:03:37 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 19:03:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Nov 2020 19:03:38 GMT
EXPOSE 80
# Thu, 05 Nov 2020 19:03:39 GMT
STOPSIGNAL SIGTERM
# Thu, 05 Nov 2020 19:03:40 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7560b97df5c18f0435e03e622714dcfb80f88d0fc32f23ce5d6efd662ae931a7`  
		Last Modified: Tue, 13 Oct 2020 03:19:17 GMT  
		Size: 35.6 MB (35602159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1312c6512e7a78551dc367f3cee76c4d95ef6993c9a150f7724a333dc518e7`  
		Last Modified: Tue, 13 Oct 2020 03:19:05 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e134fdd44fd0bf43d0e458b8a548e11e49cf1f04ae98a1e134bccbbfbd7b74`  
		Last Modified: Thu, 05 Nov 2020 19:04:51 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53990b3ad6de259d6e0b424198d108540b05be3fb00a08181efc58bf03a1c07a`  
		Last Modified: Thu, 05 Nov 2020 19:04:51 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b18757543d30f116fbdfccc67859f072e2462c198fcd8725b3c5ebd61d5ae322
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57249422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c76f90fb2a4756f29d070330cb48b229430337756ee915a33ec340b3752aa7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:47:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Nov 2020 23:02:18 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 17 Nov 2020 23:02:19 GMT
ENV NJS_VERSION=0.4.4
# Tue, 17 Nov 2020 23:02:21 GMT
ENV PKG_RELEASE=1~buster
# Tue, 17 Nov 2020 23:16:21 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 17 Nov 2020 23:16:25 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 17 Nov 2020 23:16:27 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Tue, 17 Nov 2020 23:16:28 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 17 Nov 2020 23:16:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Nov 2020 23:16:30 GMT
EXPOSE 80
# Tue, 17 Nov 2020 23:16:31 GMT
STOPSIGNAL SIGTERM
# Tue, 17 Nov 2020 23:16:32 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12faeb6250f2b5f1f2051bfbb301bd71d8310dfa19fc5b6fcaf678d1b3727d1b`  
		Last Modified: Tue, 17 Nov 2020 23:18:42 GMT  
		Size: 34.5 MB (34533072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ea2bb4d8035a3eba7c748a29730e72de92c63b956eaaadea86997a60b6e46a`  
		Last Modified: Tue, 17 Nov 2020 23:18:30 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a77136df2d668f81017b9fda7f7fbd923b8f2df1d53d05985b6b488711d605`  
		Last Modified: Tue, 17 Nov 2020 23:18:30 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0581844422e67695f7845dfc9f68bb323764eb4ce457eb8b2990e3b1b1935a`  
		Last Modified: Tue, 17 Nov 2020 23:18:30 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:2abaffbc06acaed8f7c3d0fe73674dca84b90f1c718d63227f030e1cb6f7204e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63158383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1b3b64de333c043d84d91d0dc4c8eed79de11837f87a17d33ab80964960183`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:39:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 18 Nov 2020 01:53:29 GMT
ENV NGINX_VERSION=1.18.0
# Wed, 18 Nov 2020 01:53:30 GMT
ENV NJS_VERSION=0.4.4
# Wed, 18 Nov 2020 01:53:30 GMT
ENV PKG_RELEASE=1~buster
# Wed, 18 Nov 2020 02:06:41 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 18 Nov 2020 02:06:43 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Wed, 18 Nov 2020 02:06:44 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Wed, 18 Nov 2020 02:06:45 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 18 Nov 2020 02:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 18 Nov 2020 02:06:46 GMT
EXPOSE 80
# Wed, 18 Nov 2020 02:06:47 GMT
STOPSIGNAL SIGTERM
# Wed, 18 Nov 2020 02:06:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663e524908c1169c25562a30679eb3c4e39b202cc43819cb5ff15ef3e968dca3`  
		Last Modified: Wed, 18 Nov 2020 02:08:50 GMT  
		Size: 37.3 MB (37293690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4225a81d7478ff59fb3d829249b7fc0f0bf3fc6845c79fbaa322d61dfebee4`  
		Last Modified: Wed, 18 Nov 2020 02:08:36 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ba6201405bd4f52f87b29256f0bb1bdd45089cab15b99c6d7eb3256f48e174`  
		Last Modified: Wed, 18 Nov 2020 02:08:35 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a3dc353877907586174f38361d8d71d191880e91746949a5b7f35d469020ed`  
		Last Modified: Wed, 18 Nov 2020 02:08:35 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; 386

```console
$ docker pull nginx@sha256:eaedc320c9f6134a857ea7e6bbe2387b24cf626574daf569ac37c0b912c838bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65500732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a6dd9106c1cea635ab3209afa987957e090bf943cdb9368fb5ef82acde5514`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:03 GMT
ADD file:51108b89c70ce0773c897be520c84454660f38b84ba556da49c7fe77e5d52416 in / 
# Tue, 13 Oct 2020 01:41:03 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 21:17:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Oct 2020 21:19:07 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 13 Oct 2020 21:19:08 GMT
ENV NJS_VERSION=0.4.4
# Tue, 13 Oct 2020 21:19:08 GMT
ENV PKG_RELEASE=1~buster
# Tue, 13 Oct 2020 21:20:21 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 13 Oct 2020 21:20:22 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Thu, 05 Nov 2020 18:46:28 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 18:46:28 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 18:46:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Nov 2020 18:46:29 GMT
EXPOSE 80
# Thu, 05 Nov 2020 18:46:29 GMT
STOPSIGNAL SIGTERM
# Thu, 05 Nov 2020 18:46:29 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:97e4efec21eea92209464547d0f52a0f773c505cf4ea9d8090cef667bde145b8`  
		Last Modified: Tue, 13 Oct 2020 01:48:54 GMT  
		Size: 27.8 MB (27750243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7579aecb2a012bbac5908b63f66271b9dcdbc22adf297a4158899c387f094af`  
		Last Modified: Tue, 13 Oct 2020 21:21:57 GMT  
		Size: 37.7 MB (37748339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408ca173bb1a5145dc5c098267f51574d0d36df8d54d5bcecac6a43368efbccb`  
		Last Modified: Tue, 13 Oct 2020 21:21:47 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f820cbf59fd74deb55d85db780dbfd0080be1c21ba6e2a37018ce5b7b40916b1`  
		Last Modified: Thu, 05 Nov 2020 18:47:57 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9693074ac3b0eafb80adf28edb5ffcaddb0625a3de46a272c057a806a755ad`  
		Last Modified: Thu, 05 Nov 2020 18:47:57 GMT  
		Size: 659.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:e913534e6d85f2119cf6a8cb4ca7f3994f4fef016254f8fed0d695e1eb85c38a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62037895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a344d3693cf83aa5601ec5b3243ba2c7acec286e376b2e9d43dad2d68325e30`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:24 GMT
ADD file:98a1b26b3eefd56b2867344c8c58f4bc3ef9a19c28e35c41df77ab80598d41bc in / 
# Tue, 17 Nov 2020 20:19:24 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 23:19:52 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Nov 2020 23:43:21 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 17 Nov 2020 23:43:21 GMT
ENV NJS_VERSION=0.4.4
# Tue, 17 Nov 2020 23:43:22 GMT
ENV PKG_RELEASE=1~buster
# Wed, 18 Nov 2020 00:06:33 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 18 Nov 2020 00:06:33 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Wed, 18 Nov 2020 00:06:34 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Wed, 18 Nov 2020 00:06:34 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 18 Nov 2020 00:06:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 18 Nov 2020 00:06:35 GMT
EXPOSE 80
# Wed, 18 Nov 2020 00:06:35 GMT
STOPSIGNAL SIGTERM
# Wed, 18 Nov 2020 00:06:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:071bb0a152ef32db0e7d172bcc4722a6a275885249ddb72bee023e268e82fc16`  
		Last Modified: Tue, 17 Nov 2020 20:26:34 GMT  
		Size: 25.8 MB (25777477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482ca1b388027e5c7a3f9c1beaedcda103c26d2291a080935176eeba9da7c40b`  
		Last Modified: Wed, 18 Nov 2020 00:10:00 GMT  
		Size: 36.3 MB (36258254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc32a623eb35803b73cffda6dec280c4b5e095aba215f1981f4d63803bcce49`  
		Last Modified: Wed, 18 Nov 2020 00:09:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1670c09230bd5da2dd5dc9e06deef2f18d49ec942cb853722aa5779e0c703`  
		Last Modified: Wed, 18 Nov 2020 00:09:34 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07327e440b5b1295d8098c1bd36a934d488a6d973cffa9a10545f1440ad7c7`  
		Last Modified: Wed, 18 Nov 2020 00:09:34 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:4c037e49feff8b9d6edbcd101eae220e9fc60831ae88a97efdfa739fce9016e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70189343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa64a53afc8968da81ae503dec26fc41590d345c798def96f2c91e99bf7d23e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:54 GMT
ADD file:9992867f855c9bed54df6d26f3d8076689aff8a51e808fefba7d3b66dab250e5 in / 
# Tue, 13 Oct 2020 01:38:59 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 11:02:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Oct 2020 11:44:33 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 13 Oct 2020 11:44:37 GMT
ENV NJS_VERSION=0.4.4
# Tue, 13 Oct 2020 11:44:41 GMT
ENV PKG_RELEASE=1~buster
# Tue, 13 Oct 2020 12:25:45 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 13 Oct 2020 12:25:51 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Thu, 05 Nov 2020 19:27:52 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 19:27:56 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 05 Nov 2020 19:28:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Nov 2020 19:28:07 GMT
EXPOSE 80
# Thu, 05 Nov 2020 19:28:14 GMT
STOPSIGNAL SIGTERM
# Thu, 05 Nov 2020 19:28:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:523555c6877c72cfcdec912b4d0053c298b1c97835efc7c6b0211585a06bd563`  
		Last Modified: Tue, 13 Oct 2020 01:50:10 GMT  
		Size: 30.5 MB (30517878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec7c00444ffb28b1495f4ec4d6f8d5958fa10669c5536089fdfc9f9ad148a31`  
		Last Modified: Tue, 13 Oct 2020 12:29:50 GMT  
		Size: 39.7 MB (39669305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115a2a631463568741a36820ebcc2478dbce778714153704e32941d434562e96`  
		Last Modified: Tue, 13 Oct 2020 12:29:38 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929e19180acc1a65d74e07ff697dc560d238760afb6adadc8ab66f1bfdb88e7e`  
		Last Modified: Thu, 05 Nov 2020 19:33:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b67302f4aa2d1b2a4fbe98618e423a180fac82918a68e1af990351f004ae5d`  
		Last Modified: Thu, 05 Nov 2020 19:33:07 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; s390x

```console
$ docker pull nginx@sha256:0d3ff3ec17b13cd5b8c38daeca9429ac1d646f8df4eba66ad0bf0fc8430292be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63034555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf1b67d25fa53a3a3cfdd4b31bcc0b06af698fbdc7bb6b8fdcd0ce9a8ce8d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 17 Nov 2020 20:18:29 GMT
ADD file:4a3215d1c9b4afb58053c4fff8d121547890c2a71bc027992f7f960551c6acb1 in / 
# Tue, 17 Nov 2020 20:18:34 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:56:55 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 18 Nov 2020 02:09:52 GMT
ENV NGINX_VERSION=1.18.0
# Wed, 18 Nov 2020 02:09:53 GMT
ENV NJS_VERSION=0.4.4
# Wed, 18 Nov 2020 02:09:53 GMT
ENV PKG_RELEASE=1~buster
# Wed, 18 Nov 2020 02:21:32 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 18 Nov 2020 02:21:38 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Wed, 18 Nov 2020 02:21:38 GMT
COPY file:13577a83b18ff90a0f97a15cd6380790a5f5288c651fa08708ff64d3f1595861 in /docker-entrypoint.d 
# Wed, 18 Nov 2020 02:21:39 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 18 Nov 2020 02:21:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 18 Nov 2020 02:21:40 GMT
EXPOSE 80
# Wed, 18 Nov 2020 02:21:40 GMT
STOPSIGNAL SIGTERM
# Wed, 18 Nov 2020 02:21:41 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c0d5e3cc51c0b20d3f68226f5332c9a9c2b17cce2f362ec742d4ed325ff7b530`  
		Last Modified: Tue, 17 Nov 2020 20:23:43 GMT  
		Size: 25.7 MB (25721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60013251f9ee781567d20393bc214228302751e837b71894eb21b1512db49d`  
		Last Modified: Wed, 18 Nov 2020 02:23:18 GMT  
		Size: 37.3 MB (37311247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a71de18c73c00575d38bd9ac5cb3aeb5e58d16030b0545d58ac5e96a38d2c9b`  
		Last Modified: Wed, 18 Nov 2020 02:23:13 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91367ecf1028e4270dab2b02dc1278f82b736946558ec287f23a1d45a4c76781`  
		Last Modified: Wed, 18 Nov 2020 02:23:13 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575af6ceb0a49b69b2b402e5bb04b5f70f0a7d976988215617e89b9c923f82c`  
		Last Modified: Wed, 18 Nov 2020 02:23:13 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
