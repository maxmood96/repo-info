## `kong:alpine`

```console
$ docker pull kong@sha256:a90175f1a3290007122ad5b397e4f2db67a4ca5870dc755230b6c397a08ec021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:a667daead4dbbef0fbb6da8e860fe1c16cb10ae3889f3ba02e1ed600e2f1c7cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac313c49d6bee3db1dbbf099ed50c7921640d125e75d742267ac0cf113b3160`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:08:41 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 01 Sep 2021 03:08:41 GMT
ARG ASSET=ce
# Wed, 01 Sep 2021 03:08:41 GMT
ENV ASSET=ce
# Wed, 01 Sep 2021 03:08:41 GMT
ARG EE_PORTS
# Wed, 01 Sep 2021 03:08:42 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 01 Sep 2021 03:08:42 GMT
ARG KONG_VERSION=2.5.0
# Wed, 01 Sep 2021 03:08:42 GMT
ENV KONG_VERSION=2.5.0
# Wed, 01 Sep 2021 03:08:42 GMT
ARG KONG_AMD64_SHA=ebe0cf3a3e71d202774ede5083c98e2ae39fae0459d11140f53401a66527e1b7
# Wed, 01 Sep 2021 03:08:42 GMT
ENV KONG_AMD64_SHA=ebe0cf3a3e71d202774ede5083c98e2ae39fae0459d11140f53401a66527e1b7
# Wed, 01 Sep 2021 03:08:43 GMT
ARG KONG_ARM64_SHA=131964ce443f2d08dc98191fcc442867f2dee2f741ccee9cc519bb99c765f3cf
# Wed, 01 Sep 2021 03:08:43 GMT
ENV KONG_ARM64_SHA=131964ce443f2d08dc98191fcc442867f2dee2f741ccee9cc519bb99c765f3cf
# Wed, 01 Sep 2021 03:08:51 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 01 Sep 2021 03:08:51 GMT
COPY file:a9828df20ead648b4c991bfb67a40d0065e248e50a2ae98fad0104e78f32d234 in /docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:08:51 GMT
USER kong
# Wed, 01 Sep 2021 03:08:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:08:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 01 Sep 2021 03:08:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Sep 2021 03:08:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 01 Sep 2021 03:08:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a932a260c1e4852852f30dfd019cb0eaeca493933da107b49b478f97a8114a`  
		Last Modified: Wed, 01 Sep 2021 03:09:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af18b1a4934e2c5e54790d320d17240ba331b21f0df9b2d4892f9b8a5a57c5aa`  
		Last Modified: Wed, 01 Sep 2021 03:09:53 GMT  
		Size: 46.7 MB (46727187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97ef9b6bde488c17df64ac1a14770099af9f764e728f626da456fcd3cff2afc`  
		Last Modified: Wed, 01 Sep 2021 03:09:45 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8231711dae245456227c2b5eb1fe12f907f9fd9c0205a09627fc9430d2ab9765
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48937742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325cf6127197d92d3cb30f7f71cc004eb1f74955a5c067d775da6f299074785d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 13:09:28 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 01 Sep 2021 13:09:28 GMT
ARG ASSET=ce
# Wed, 01 Sep 2021 13:09:29 GMT
ENV ASSET=ce
# Wed, 01 Sep 2021 13:09:29 GMT
ARG EE_PORTS
# Wed, 01 Sep 2021 13:09:29 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 01 Sep 2021 13:09:29 GMT
ARG KONG_VERSION=2.5.0
# Wed, 01 Sep 2021 13:09:29 GMT
ENV KONG_VERSION=2.5.0
# Wed, 01 Sep 2021 13:09:30 GMT
ARG KONG_AMD64_SHA=ebe0cf3a3e71d202774ede5083c98e2ae39fae0459d11140f53401a66527e1b7
# Wed, 01 Sep 2021 13:09:30 GMT
ENV KONG_AMD64_SHA=ebe0cf3a3e71d202774ede5083c98e2ae39fae0459d11140f53401a66527e1b7
# Wed, 01 Sep 2021 13:09:30 GMT
ARG KONG_ARM64_SHA=131964ce443f2d08dc98191fcc442867f2dee2f741ccee9cc519bb99c765f3cf
# Wed, 01 Sep 2021 13:09:30 GMT
ENV KONG_ARM64_SHA=131964ce443f2d08dc98191fcc442867f2dee2f741ccee9cc519bb99c765f3cf
# Wed, 01 Sep 2021 13:09:37 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 01 Sep 2021 13:09:38 GMT
COPY file:a9828df20ead648b4c991bfb67a40d0065e248e50a2ae98fad0104e78f32d234 in /docker-entrypoint.sh 
# Wed, 01 Sep 2021 13:09:38 GMT
USER kong
# Wed, 01 Sep 2021 13:09:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Sep 2021 13:09:38 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 01 Sep 2021 13:09:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Sep 2021 13:09:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 01 Sep 2021 13:09:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834874c5e974b53eb28baf25287cb6506a1ba5b4e01ff118aaa9566fcecb5c39`  
		Last Modified: Wed, 01 Sep 2021 13:10:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f1885bae9c378b0ed22b0f54882317aa2b369c3437d48dde9383bde00fe9cc`  
		Last Modified: Wed, 01 Sep 2021 13:10:55 GMT  
		Size: 46.2 MB (46223868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749c3863a80bc68fa2ffebe71f27d856b6914678264e891679ad6554ec59c613`  
		Last Modified: Wed, 01 Sep 2021 13:10:44 GMT  
		Size: 735.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
