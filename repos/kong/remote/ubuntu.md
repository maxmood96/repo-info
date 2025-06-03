## `kong:ubuntu`

```console
$ docker pull kong@sha256:b2980ac91056bcc9cbf593b2b3d6a8c458cc134304b4d83bc4c93a6449f18df7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:28bd5b80103fc3e92def8f5a425ae39e81cddcb5473055d43182f9f6a7e6cb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a23e5674d9d5c548f68d00728660196cf3f3c770d3f1bfa57930b0f0bebaabd`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0889df95b3464c89349b853285c0cba2891dd4e40588ce2b1b2110c171fd7a98`  
		Last Modified: Tue, 03 Jun 2025 13:32:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8f1a58e16fa22c5d9638bce323255c0a0cd09394f497b5ecd6795e9e616c4c`  
		Last Modified: Tue, 03 Jun 2025 13:32:36 GMT  
		Size: 90.6 MB (90573893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3402ea08968303b1193be322252f5998757a6649e4413facbf52521d076607bb`  
		Last Modified: Tue, 03 Jun 2025 13:34:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:ee73791c0ad1217f4c5534b1451a443c1c9ed24eb4c82f279b0afc29ca966591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7216d51e0332f9d9036c726489b4f2dd9d461489cbdb7c67d72cb28a73f1b88`

```dockerfile
```

-	Layers:
	-	`sha256:59186a39b9e3a3bd132fb688c6ab86a90b34939916de81ab7223975fda23ca2c`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 5.3 MB (5314069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fb761a8103dfd15789abe83517e58fb2d8517276ecb312c199d4c42a61a40c`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:169b01897e77c6c007ac63ee0a38abcf47657f501d5f2da0f9fd24c25237a7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118738681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff986ab321efcc553232dd2440d239b623b48b1863a86bd9c56092b966f1a5`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3741458962a2d3c83383c586049cbbb2acf5695765a6a7c77cf91a575a6589`  
		Last Modified: Tue, 03 Jun 2025 13:32:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf683f0dcc4dea9277486a6777b482a515b8a54a28634ab48d346000dc37a498`  
		Last Modified: Tue, 03 Jun 2025 13:34:24 GMT  
		Size: 89.9 MB (89885493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac77cbd262d312d23890bf1bcc89b02b8242f3d63cf01545b1d629ea94ba578`  
		Last Modified: Tue, 03 Jun 2025 13:32:34 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f8c6d404cc7f7c9671a00d63445763276ac5bd44c15766ab57676659fa966e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643f2d4683b1d19d9745e756d5073118ad0bd87ff48acdaf19bd271395dc32eb`

```dockerfile
```

-	Layers:
	-	`sha256:d66e6888cae9578709c0eacd85194caeed33e9f08116865a15b0e44db2f7a5e9`  
		Last Modified: Tue, 03 Jun 2025 05:03:10 GMT  
		Size: 5.3 MB (5321236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29c29c628175089a96764c8a0cd4368a9c4fa3f4ceb053f947dc9fdeabe6b16`  
		Last Modified: Tue, 03 Jun 2025 05:03:10 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json
