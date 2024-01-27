## `kong:alpine`

```console
$ docker pull kong@sha256:cbb0b61a591c9484cbf2a37b5850057e54d4dc96f8c07c07001cf1e47315829d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:c4a028c24c2e8b5d81d686a7c411ec4c4f80f1dcd495ea6c1026e4b7b8f8ab29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34231634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92def505322dce3d2b96b9ad20c95b6b5cc025658a2fa427c9fd73776c59dc8b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:50:39 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_VERSION=3.3.1
# Sat, 27 Jan 2024 03:50:39 GMT
ENV KONG_VERSION=3.3.1
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:39 GMT
ENV KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:39 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:50:39 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:50:39 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:50:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:50:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:50:46 GMT
USER kong
# Sat, 27 Jan 2024 03:50:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:50:46 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:50:46 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:50:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:50:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2059c54846f7238a7e9e662c2ddd540de2c4db29fab44c43fbe070b39b8b61`  
		Last Modified: Sat, 27 Jan 2024 03:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c3036110cfbae400e5b2fd68ce10ecf07c0cad0a9a0754f202ef6114c8a5c`  
		Last Modified: Sat, 27 Jan 2024 03:52:03 GMT  
		Size: 30.9 MB (30850943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713fc864f01da83252ecef138198826f49c9ca9603f4d8cc9a7b2f5e2a8bcd3e`  
		Last Modified: Sat, 27 Jan 2024 03:51:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
