## `nginx:stable-bullseye`

```console
$ docker pull nginx@sha256:0ffb12ab530e3a2fb77753e4733210f1e31283e002cfe1c64bc6986d1189174c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:stable-bullseye` - linux; amd64

```console
$ docker pull nginx@sha256:f67fb2924e03b82df90d578ff9676cb2316f15c407b267a52294914e55612c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57026451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f373f7a623e7d55454a59190b2d50e8a1d92faa8626fa48b4153c63a4872cff6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfddd3151d4b39c35f2d4912fe9659f0d2e0839c25687dff00f4607b670eebe`  
		Last Modified: Fri, 12 Jan 2024 00:22:12 GMT  
		Size: 25.6 MB (25604750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a14c9c58a700403015da2351fcaa45183987ddfaa8a3e565f21a922433d7c7d`  
		Last Modified: Fri, 12 Jan 2024 00:22:11 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aff079cc60f1a59e7141c3eee47a2080ed8dddb5ba6c32decb82e526d2c884`  
		Last Modified: Fri, 12 Jan 2024 00:22:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93498c6629aae7250fd1e8b004e5e3f92836b0a70f245b927c1486a47af805e2`  
		Last Modified: Fri, 12 Jan 2024 00:22:11 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67e21d7eabc78c6aa644b61bbafca6984f58c395044943f638e7ce7c3eed82b`  
		Last Modified: Fri, 12 Jan 2024 00:22:12 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:905dd4bc23ca3ee19fef9a0cecb0d926d50fe20fd6b095f44cca7b95f1567f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49f38c9c62c3d4e3a54348237eb51b2f735fbe321344c843f6de3a3d55d86b6`

```dockerfile
```

-	Layers:
	-	`sha256:5e3c5299f5a01abc0dcdd88f61644286f3aaed43dde22fc862d50a58b1388410`  
		Last Modified: Fri, 12 Jan 2024 00:22:11 GMT  
		Size: 2.6 MB (2587753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fdcc0d573927b17b46ea02484efd197440069f02eff441892ce2f983640fa5`  
		Last Modified: Fri, 12 Jan 2024 00:22:11 GMT  
		Size: 27.3 KB (27326 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; arm variant v5

```console
$ docker pull nginx@sha256:7a85506770f1127834c1b7a71a5bd983f22118b9fd9d8d26f8795856236beaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53688266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1eaadf8ae584e3571ae066f24a449930614415e74e82a09f98ad9280ddcedfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bae347613d4dc9215e0232efb155a55682c4cc34e05556811208fc9fed4445`  
		Last Modified: Wed, 20 Dec 2023 20:35:02 GMT  
		Size: 24.8 MB (24763234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105a2abd3e3a087c1f417184f0e47602d5b4106911e820bddecfad59b08ba65c`  
		Last Modified: Wed, 20 Dec 2023 20:35:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7630b1dbc2954b5958436df03102db0bdcecebb7c247a9df4626b2d6449f1030`  
		Last Modified: Wed, 20 Dec 2023 20:35:01 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c85092197cbeb8595fb4e662852b540f45855aca2d8946f00e70b4942f61f`  
		Last Modified: Wed, 20 Dec 2023 20:35:01 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26eccf0e7fa00b505af5d7279c1b2d5bcb850347a0890fd51d37bbb02c1ad90`  
		Last Modified: Wed, 20 Dec 2023 20:35:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:6f391bd4fd340b66af29d0872f0c65c141743a62a5f13fcbb01f726d472939fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2597912e0f4dbe21d4c9b2d8bdd6050a21c12b8797d8e74428fd58994e2aa47d`

```dockerfile
```

-	Layers:
	-	`sha256:361401454ada78ca31c4a29b34aaed843512fc74b6b08ee95f0c51e1c2ce6603`  
		Last Modified: Wed, 20 Dec 2023 20:35:01 GMT  
		Size: 27.0 KB (27030 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5553cfeb6c045252a0f4ac6d50ac92e61dcfcbd698754e364877120bca4280eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48165eae0e6ba1f9a8c0b24115eaa1ec16d5977f063c8bd1e296858a582ee515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:19ccf4d6cc6956e4a5522352be94632923aa376a9939a4f45428a4f304c73bc8`  
		Last Modified: Tue, 19 Dec 2023 02:12:33 GMT  
		Size: 26.6 MB (26578972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a409abaf47aa58d76d5c7488c3629fc3d190f58cb824296c6e1569c54163cbd`  
		Last Modified: Wed, 20 Dec 2023 23:23:41 GMT  
		Size: 23.9 MB (23882646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fad3eaca1101e4fbd84d6b069bb54a1e5368292906e173c1accdd73aa99fc4`  
		Last Modified: Wed, 20 Dec 2023 23:23:40 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b203e8ae4cc9c6ed046c0e18c3b958148f369024c788ac8a17d21277b9594`  
		Last Modified: Wed, 20 Dec 2023 23:23:40 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a8ba84dd5fd1c6bc8174d64c9ea4e6645f6d9ddd424bffa3bca7be1eac8d3c`  
		Last Modified: Wed, 20 Dec 2023 23:23:40 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5844eed59e59de8f37613a0d8f6687532743bcaf9cdadf6c12e9350e581964`  
		Last Modified: Wed, 20 Dec 2023 23:23:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:cc0a72b3f566618eed25adf2a92b121a7ccff9aa96cef93e9adbfac4eefe2d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284385e487216a1f92e88616763a7517c5e7dc65620cc01dc59edf721a16be54`

```dockerfile
```

-	Layers:
	-	`sha256:459c6720826b995a243eb9d2cbe9b1e554854165e90a6d830d8718b90625d245`  
		Last Modified: Wed, 20 Dec 2023 23:23:40 GMT  
		Size: 2.6 MB (2598930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfe960d546ec4306cb1fe6b4ee83adac8363b9e1933c6275dbd92db08efd28`  
		Last Modified: Wed, 20 Dec 2023 23:23:40 GMT  
		Size: 27.2 KB (27245 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:ce84c845eac32f06043eaa50b3e6245c1848dc5ffb346804ee7909b46d18091e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55599278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410d5706901d3feaf67137c8f2901def463999b06abbb108edfccccaba77e5dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abd21046c589d49064b2876d21806d3a991215b99202ad6c3771833b577f4f`  
		Last Modified: Wed, 20 Dec 2023 22:36:24 GMT  
		Size: 25.5 MB (25531479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a119ee288c30b459c6b6ec190d11efead5b099d9be3789e43cc791cc8a553b3`  
		Last Modified: Wed, 20 Dec 2023 22:36:23 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cab96456ea5ffc1a923b3cd28375127f6d20cc1ad3efd718e678543c5ef9948`  
		Last Modified: Wed, 20 Dec 2023 22:36:23 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4ae15abc2be1b886257d8afd770b3d47f5164018b122b86bbd7ae2b28457e9`  
		Last Modified: Wed, 20 Dec 2023 22:36:23 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e27d996f24965ee5863eb52efcd865729c82dc2a913edb5b1538cbefde0c608`  
		Last Modified: Wed, 20 Dec 2023 22:36:24 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:9bf21b7568ad9ec2c3300cbcb2246cfe5ace9e1747b2deebdab00119a9a47605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ee5b265a211ad946482bb8d91bc09cdf7618a87e2124fae9a19e800ee655cd`

```dockerfile
```

-	Layers:
	-	`sha256:dd1ef3f19343170b333815da9c0cae551c1ab8ff2b40140cd5b2f24a774a4795`  
		Last Modified: Wed, 20 Dec 2023 22:36:23 GMT  
		Size: 2.6 MB (2588112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc13df8e58f3aaf509790bb03d36e649667434f0dc2637de6561bf1671e53ca6`  
		Last Modified: Wed, 20 Dec 2023 22:36:23 GMT  
		Size: 27.2 KB (27173 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; 386

```console
$ docker pull nginx@sha256:4f0375f95c7466384b8bd8ddf11d26fe7cfa0d8388842cb7bbf04a57d528eaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58953264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bdf3a638592bfdd99abe061d2c8c886ee9a2a7dbc70684fbc28adbec538dbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a001517c87d4542e6d56eb19a3005910a5924085fff47840daf3216253a0103a`  
		Last Modified: Fri, 12 Jan 2024 00:25:20 GMT  
		Size: 26.5 MB (26546846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710e0f5fb8eecdaaaa4cad65ae0f817d7c17dfaa93b68ef27e33f90b2067070`  
		Last Modified: Fri, 12 Jan 2024 00:25:19 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45163fa708ec505a5a43e9158516a38ef2dcd83f17a7ce374925ba73e846002`  
		Last Modified: Fri, 12 Jan 2024 00:25:19 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be51ac05b66ade3888dda2a223c1d703bf198b060dcf9bf658cf7addfa1eea`  
		Last Modified: Fri, 12 Jan 2024 00:25:19 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a7583077325c1b3c3e258f06173d794ec641eab61bbcd0ef3b0328ad15e5a4`  
		Last Modified: Fri, 12 Jan 2024 00:25:20 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:5525424bb0ec8d029bbc2ca01271efc3529285340a9183e0c5dbc8543e95eb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c9ec3f7b17a4e19f20fbab527a7de3c42b68d948983e9ac86345759660a052`

```dockerfile
```

-	Layers:
	-	`sha256:43ec362c9faf894148270ec703036b61c30b7aae3d111193283103719ad49e44`  
		Last Modified: Fri, 12 Jan 2024 00:25:19 GMT  
		Size: 2.6 MB (2593579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c75a83d5b1fc450183991f82ac17444664b027259ee9f0e0794ac56d8e41925`  
		Last Modified: Fri, 12 Jan 2024 00:25:19 GMT  
		Size: 27.3 KB (27287 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; mips64le

```console
$ docker pull nginx@sha256:4f5b6c71428b4070eb27b8526758a66d4f430e654e3e3de6a33b5479d3df7f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55120551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69fc155abf9f79a986a3693f786a9d919ada78896df8adda991ba4f966b9850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:dcc77071aa6c677714230fd845d154c00ba6ba34a78f8f1073c224e90f17f543 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f9454980ac665cb2d7641130c738c2054ef7a7516386fc6742b46b5b60dd93ad`  
		Last Modified: Tue, 19 Dec 2023 02:26:03 GMT  
		Size: 29.6 MB (29635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506a020fc16aa43a2da98d716b691bea1548821b0d80c537de01cff4240c6b9`  
		Last Modified: Thu, 21 Dec 2023 15:35:04 GMT  
		Size: 25.5 MB (25480816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a3b88e0d2ea76d3ebb3d49c7c1fc78e5c9700a68b63a727c34adbeb0d9911`  
		Last Modified: Thu, 21 Dec 2023 15:35:01 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14edbc72c7c98e27c2361252cc5d601cb9861e160b3d1c2ce9a0525d077a0f8f`  
		Last Modified: Thu, 21 Dec 2023 15:35:01 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7602ce84f4e95db449f801a480efea2619d2986769de836eb9077cb1e904ea8`  
		Last Modified: Thu, 21 Dec 2023 15:35:01 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4813961c7545ab63b1ff3d849d0806aef95b479ddb7f5315ee8ba9038c23dce`  
		Last Modified: Thu, 21 Dec 2023 15:35:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:a3b667df9ffd32a52f6ef2883b43c3f7d03f16792f77291290d6d00d962d25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd3cfe6b189175150b975dc3b7461eae3826fe93329dbd19dd3779acd3e79e4`

```dockerfile
```

-	Layers:
	-	`sha256:e23501f03020ad98c3a17488fcecd3ef47ad3e299e17984248c0205c2c2f5045`  
		Last Modified: Thu, 21 Dec 2023 15:35:01 GMT  
		Size: 27.0 KB (27019 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; ppc64le

```console
$ docker pull nginx@sha256:0408a9896355d0157c236cffb92491fb1f23b872ac25075b00fa84f0ad79ea82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62769535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c5d89372d532659401e36c1698057a2793439e6984bf48b81b29f35e7c0fed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f3379e53b50e63b98865850b6d18add7e77e7eb3f789e0be905e195042f54f`  
		Last Modified: Wed, 20 Dec 2023 21:23:56 GMT  
		Size: 27.5 MB (27471979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9215f5bb2f789dd8ddf905dbea28b3e7b3ad0f29cb5f6c2277c4d4e94e825f69`  
		Last Modified: Wed, 20 Dec 2023 21:23:55 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489d768e67d43d874b88f8850855cf95574966e7ffb9c0de63fdc58a9e6b6837`  
		Last Modified: Wed, 20 Dec 2023 21:23:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78018688747cacff90bfc8482b3ce67a36b0705406a5521a89d700a593b54c29`  
		Last Modified: Wed, 20 Dec 2023 21:23:55 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a780a5890e8a83cc1ae602f947073b3d9908b0fbc1cf3c148b8f9ce3127a7c`  
		Last Modified: Wed, 20 Dec 2023 21:23:56 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:2da85f3ac21ce61735b5f07c9b98a272e8790aedc98114e77447751c55747c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0594f96bd2d3622e392d228a05bd0087ca37660625f740bca3a25c7a548e504e`

```dockerfile
```

-	Layers:
	-	`sha256:7cd41d471d54a84c0b966ff052f62ceb35d9a590ec8298cfa7ac47b13b173991`  
		Last Modified: Wed, 20 Dec 2023 21:23:55 GMT  
		Size: 2.6 MB (2601167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d4a68fcee16a17605babd8112aed342bc281342e4a0834c42ba0313bcce3ef`  
		Last Modified: Wed, 20 Dec 2023 21:23:55 GMT  
		Size: 27.2 KB (27209 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; s390x

```console
$ docker pull nginx@sha256:eff553fe6efc37005cac4c734ef35f7645d3e36d0b40eb80458fae5b1e1f95e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55075384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859d75e12b327471f4e3bcd0f72623ed697c1bb9246474c20d792a29d8d43b09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290d839981aa55d9162356d521b02caba915d724ef7c009957f0469321383341`  
		Last Modified: Wed, 20 Dec 2023 21:27:12 GMT  
		Size: 25.4 MB (25414623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f545eaf7bc896c58c3f3cb6da64367965e74a2c8cb96e6c5db64630594c3ce`  
		Last Modified: Wed, 20 Dec 2023 21:27:11 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c506f6b2d95688df5f1ac5773fc196341ed3dfb1d0fdd06eec41c874f46d9539`  
		Last Modified: Wed, 20 Dec 2023 21:27:12 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194f476199a230a8fe02571f59df0e46d01710dae29715a448102047534b6678`  
		Last Modified: Wed, 20 Dec 2023 21:27:11 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82f3e8784cd60c311b2da2b9516e3e4fc926db6646cfab2056f166b9ea52c6`  
		Last Modified: Wed, 20 Dec 2023 21:27:12 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:d6f51c58a018794c36d47a6e7fcafc096af171f8da125e7159cc1afbcbef0356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449096d754caadd622d7d662b789b21177e5c89dc3b947828147d84028e83428`

```dockerfile
```

-	Layers:
	-	`sha256:8f7e41cd528c9a800825af037151223eb679c927b16cd1f5d8d889c49ce8c6ac`  
		Last Modified: Wed, 20 Dec 2023 21:27:11 GMT  
		Size: 2.6 MB (2596524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c74dfd751d2fe2e1411226ca4aa11f3db9d68c41ddf078adaec596869e93427`  
		Last Modified: Wed, 20 Dec 2023 21:27:11 GMT  
		Size: 27.2 KB (27159 bytes)  
		MIME: application/vnd.in-toto+json
