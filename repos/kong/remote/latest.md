## `kong:latest`

```console
$ docker pull kong@sha256:f753cd11833984d5b730b6453e1b37a6bda957bd348e6d3b94012998e171e986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:77afc9416f5d2f8d9df8475489b81124c9ea51f9a795874b94ddb026a1277a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f819da0f01e7ccc3f84d99091d19e9b2c306d5a32f5f40750509e04f035cc43a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:49:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 04 May 2023 07:49:24 GMT
ARG ASSET=ce
# Thu, 04 May 2023 07:49:24 GMT
ENV ASSET=ce
# Thu, 04 May 2023 07:49:24 GMT
ARG EE_PORTS
# Thu, 04 May 2023 07:49:24 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Mon, 22 May 2023 20:20:02 GMT
ARG KONG_VERSION=3.3.0
# Mon, 22 May 2023 20:20:02 GMT
ENV KONG_VERSION=3.3.0
# Mon, 22 May 2023 20:20:02 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Mon, 22 May 2023 20:20:02 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Mon, 22 May 2023 20:20:48 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Mon, 22 May 2023 20:20:49 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Mon, 22 May 2023 20:20:49 GMT
USER kong
# Mon, 22 May 2023 20:20:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:20:49 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 May 2023 20:20:49 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 May 2023 20:20:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 22 May 2023 20:20:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4452e2a99e08079eada765eaec98220af45483cd8a0e7809ca19f969da460e32`  
		Last Modified: Thu, 04 May 2023 07:50:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9a936bd7cc5b4fd65a932689dbf1b99af396d857f0a16e3b404e8ffac8ea9`  
		Last Modified: Mon, 22 May 2023 20:21:54 GMT  
		Size: 50.9 MB (50879640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184c4befd98b6832d330e8c5ab7fd227ca4a0332ba1216c82b4cc141e0f4897a`  
		Last Modified: Mon, 22 May 2023 20:21:46 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
