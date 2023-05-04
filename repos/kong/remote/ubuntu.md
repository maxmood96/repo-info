## `kong:ubuntu`

```console
$ docker pull kong@sha256:006ccabcf048b8cfb4d8033d7c01e1e5b11cdd7adda983f4e219ec6e088873a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f5f51af49fa1f5a7600e60bb51ebd760b16fd020bb16bba2b70d36a54f3d6ac8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74381601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a4a92323976685af4f320261472e8c4575583169192c82d27e246681fc216`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Sat, 25 Mar 2023 00:51:10 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 25 Mar 2023 00:51:10 GMT
ARG ASSET=ce
# Sat, 25 Mar 2023 00:51:10 GMT
ENV ASSET=ce
# Sat, 25 Mar 2023 00:51:10 GMT
ARG EE_PORTS
# Sat, 25 Mar 2023 00:51:11 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 25 Mar 2023 00:51:11 GMT
ARG KONG_VERSION=3.2.2
# Sat, 25 Mar 2023 00:51:11 GMT
ENV KONG_VERSION=3.2.2
# Sat, 25 Mar 2023 00:51:11 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 25 Mar 2023 00:51:11 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 25 Mar 2023 00:52:03 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 25 Mar 2023 00:52:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 25 Mar 2023 00:52:04 GMT
USER kong
# Sat, 25 Mar 2023 00:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Mar 2023 00:52:04 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 25 Mar 2023 00:52:04 GMT
STOPSIGNAL SIGQUIT
# Sat, 25 Mar 2023 00:52:04 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 25 Mar 2023 00:52:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a798f30a08e58465197ea53af5348cb1920b409dce739c8c1191fa526b779c26`  
		Last Modified: Sat, 25 Mar 2023 00:52:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192c4afa29b67585a708114ac6e302a8de969f95b6037af093514f0b41e1a873`  
		Last Modified: Sat, 25 Mar 2023 00:52:58 GMT  
		Size: 44.0 MB (43950354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8497c811ba9ee1b3aa10434828370b73152317680fd95a5b7718672c3cfb2b2c`  
		Last Modified: Sat, 25 Mar 2023 00:52:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:331455622bce663694cf274fa5acc68a84bea80ecbe4b4b7403ec54eab362d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78563017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cb403e2e2a3e8ccb433f50a8ae3f79029e5ae441e50157c90bc9fca8c52cfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:44:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 04 May 2023 03:44:59 GMT
ARG ASSET=ce
# Thu, 04 May 2023 03:44:59 GMT
ENV ASSET=ce
# Thu, 04 May 2023 03:44:59 GMT
ARG EE_PORTS
# Thu, 04 May 2023 03:44:59 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 04 May 2023 03:44:59 GMT
ARG KONG_VERSION=3.2.2
# Thu, 04 May 2023 03:44:59 GMT
ENV KONG_VERSION=3.2.2
# Thu, 04 May 2023 03:44:59 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Thu, 04 May 2023 03:44:59 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Thu, 04 May 2023 03:45:16 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 04 May 2023 03:45:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 04 May 2023 03:45:17 GMT
USER kong
# Thu, 04 May 2023 03:45:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 May 2023 03:45:17 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 04 May 2023 03:45:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 May 2023 03:45:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 04 May 2023 03:45:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aead6b4c2aa9f393a63e92067a6a16c0f1527ee558eda6b45181f820bcf1f61`  
		Last Modified: Thu, 04 May 2023 03:45:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e562bf9fba3e3ac55944fd6b19bac4ffac0d4bee31828b1d3cdca127298dca6`  
		Last Modified: Thu, 04 May 2023 03:45:45 GMT  
		Size: 50.2 MB (50172295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b47e7a18f6ca88337071e2830f034ea6b85f3b0a4d3d980a63b3c7d5309394`  
		Last Modified: Thu, 04 May 2023 03:45:39 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
