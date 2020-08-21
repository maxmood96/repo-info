## `kong:alpine`

```console
$ docker pull kong@sha256:da6a051abc306094600d9aeee1acf68361966450f516de38255125469b2d8f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:723bf97cfdeaa1a406935e1759c2f592d327566d659b30202f80da02c78ffc62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53144837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62a8307bf7fd7fe6031f9b0ff3763a461143e6da341da33ea955ee31877ba02`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 20 Aug 2020 23:19:49 GMT
ARG KONG_VERSION=2.1.3
# Thu, 20 Aug 2020 23:19:49 GMT
ENV KONG_VERSION=2.1.3
# Thu, 20 Aug 2020 23:19:49 GMT
ARG KONG_SHA256=2f2a73d468d95f3ded495aa4199b55d2148d1ad5cb5050372621a1768b34ba8a
# Thu, 20 Aug 2020 23:19:55 GMT
# ARGS: KONG_SHA256=2f2a73d468d95f3ded495aa4199b55d2148d1ad5cb5050372621a1768b34ba8a
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 20 Aug 2020 23:19:55 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 20 Aug 2020 23:19:55 GMT
USER kong
# Thu, 20 Aug 2020 23:19:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Aug 2020 23:19:56 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 20 Aug 2020 23:19:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Aug 2020 23:19:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f67e15df63b8d20592937e5d3cc7d55d5c2e0e3d5cf38f8cdc640bdc919394`  
		Last Modified: Thu, 20 Aug 2020 23:21:38 GMT  
		Size: 50.3 MB (50330658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985f1bf5706fb044dc193de9b6d0007ac3a07720ac24a5d500937e8dcabe1acf`  
		Last Modified: Thu, 20 Aug 2020 23:21:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
