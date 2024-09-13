## `kong:ubuntu`

```console
$ docker pull kong@sha256:01eb3c47d518bd4489f8c15733acbfef86c97a3d79fea092eadfab16756ced42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:86ee85a52d7f58fec66ea0b16e43787d86143c6e8b27bf42f3817ee658d96c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117523680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d691bb904a74a07e54ae9804c2c916a2f96726d2633a1652bb0e87c1b9fa9e0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88de79b63b327e02d1e4edc3d86b7b8613d000a254f79e4f353323fac71cb87`  
		Last Modified: Thu, 12 Sep 2024 20:02:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe98956cff46589a96a030024b8880f66343231a416c23365eede3178673ce22`  
		Last Modified: Thu, 12 Sep 2024 20:02:25 GMT  
		Size: 88.0 MB (87986369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a92fdccec3c04bbf80998974de04f326adcc2aec1d63b6b797c078da0d43431`  
		Last Modified: Thu, 12 Sep 2024 20:02:22 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:93ee90c02e02547d25b63bf376816d3976da3c112853cf36833d88ed793b82a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6eba9d9e33c01090908ff11e04585548c4f85e0eccf3591173772bc6f3394e`

```dockerfile
```

-	Layers:
	-	`sha256:296ac80e34db848c90c266673259b3b26f55fff1c8f7d9193169ed7a2a81f78c`  
		Last Modified: Thu, 12 Sep 2024 20:02:23 GMT  
		Size: 5.2 MB (5212178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4cd15dfbdfe56b67140f0aba0ccc450ed520bc40a172a21965fb667f099f08`  
		Last Modified: Thu, 12 Sep 2024 20:02:22 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4c92c934470f118aff2da60838cce9fe5165228b9ffedfeb1ccd537149c52371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114629268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13ac6286486639374a9e3692fd430312370c5a7ffc7abea28d6f5a251014d89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744e2eddc139696c125eba2168bf743f4a18588e87f9e370fd53f987bb1c1db8`  
		Last Modified: Thu, 12 Sep 2024 20:21:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e96cb10c1cc2413b862cf77f4e1bea93f20d28cf194ff72f2ee5b7787f1f4c1`  
		Last Modified: Thu, 12 Sep 2024 20:21:40 GMT  
		Size: 87.3 MB (87269298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac7ce5774f8ab147bd0c0377ae8b62c6d97c29e12d93e6c2ee0df610c8e242`  
		Last Modified: Thu, 12 Sep 2024 20:21:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:322fd68ac1a814fe4b9f6e463d21338be709c7ebd761a6b2d239e5f0897f3958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bbc1921b9cfe6af5b80ef75aa06a10e45103f7040cb4258796c12bf71a423a`

```dockerfile
```

-	Layers:
	-	`sha256:cf37f26f1a66322c0087658f3a8e3d318e0af04b25f3c52bd84b6b636f94cd14`  
		Last Modified: Thu, 12 Sep 2024 20:21:38 GMT  
		Size: 5.2 MB (5218546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49dfca2d1c4eeb659ef12f9b5ae442b8238984b77b2bf5d6c990d8858df9787d`  
		Last Modified: Thu, 12 Sep 2024 20:21:38 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
