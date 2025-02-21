## `kong:ubuntu`

```console
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json
