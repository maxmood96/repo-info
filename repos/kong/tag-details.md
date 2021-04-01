<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2`](#kong2)
-	[`kong:2.0`](#kong20)
-	[`kong:2.0-centos`](#kong20-centos)
-	[`kong:2.0-ubuntu`](#kong20-ubuntu)
-	[`kong:2.0.5`](#kong205)
-	[`kong:2.0.5-alpine`](#kong205-alpine)
-	[`kong:2.0.5-centos`](#kong205-centos)
-	[`kong:2.0.5-ubuntu`](#kong205-ubuntu)
-	[`kong:2.1`](#kong21)
-	[`kong:2.1-alpine`](#kong21-alpine)
-	[`kong:2.1-centos`](#kong21-centos)
-	[`kong:2.1-ubuntu`](#kong21-ubuntu)
-	[`kong:2.1.4`](#kong214)
-	[`kong:2.1.4-alpine`](#kong214-alpine)
-	[`kong:2.1.4-centos`](#kong214-centos)
-	[`kong:2.1.4-ubuntu`](#kong214-ubuntu)
-	[`kong:2.2`](#kong22)
-	[`kong:2.2-alpine`](#kong22-alpine)
-	[`kong:2.2-centos`](#kong22-centos)
-	[`kong:2.2-ubuntu`](#kong22-ubuntu)
-	[`kong:2.2.2`](#kong222)
-	[`kong:2.2.2-alpine`](#kong222-alpine)
-	[`kong:2.2.2-centos`](#kong222-centos)
-	[`kong:2.2.2-ubuntu`](#kong222-ubuntu)
-	[`kong:2.3`](#kong23)
-	[`kong:2.3-alpine`](#kong23-alpine)
-	[`kong:2.3-centos`](#kong23-centos)
-	[`kong:2.3-ubuntu`](#kong23-ubuntu)
-	[`kong:2.3.3`](#kong233)
-	[`kong:2.3.3-alpine`](#kong233-alpine)
-	[`kong:2.3.3-centos`](#kong233-centos)
-	[`kong:2.3.3-ubuntu`](#kong233-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0`

```console
$ docker pull kong@sha256:bbb13e25c34a5c4e96332d2b50eb3fcc32d7946a410b13d056ad905c9ec65325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0` - linux; amd64

```console
$ docker pull kong@sha256:cbd33d90779eb12eb7e613d8bdb8c4ab2007d307e8f50172b3673ff1a631fc0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52769878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e139591360b0b1a90c7ca74ee8284f71a1f0851b4a28f8d04135c4e64a51f8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:26:15 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:26:15 GMT
ARG KONG_VERSION=2.0.5
# Thu, 01 Apr 2021 14:26:15 GMT
ENV KONG_VERSION=2.0.5
# Thu, 01 Apr 2021 14:26:15 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Thu, 01 Apr 2021 14:26:16 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Thu, 01 Apr 2021 14:26:22 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Thu, 01 Apr 2021 14:26:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:23 GMT
USER kong
# Thu, 01 Apr 2021 14:26:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5615f2d578be1c601e3c8f7f5caa944e8b35a9dcccc414bbb4a83452f15f823`  
		Last Modified: Thu, 01 Apr 2021 14:28:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f6a30785898fddd810f8b06483b8b88ff2a52eb0524b873ebcae3086a6f270`  
		Last Modified: Thu, 01 Apr 2021 14:28:56 GMT  
		Size: 50.0 MB (49953667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3c1a6567c6914fd362c0b3d6800fd976c155e704650cc35d2c866df982bf88`  
		Last Modified: Thu, 01 Apr 2021 14:28:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-centos`

```console
$ docker pull kong@sha256:7a6ec5d8213e47be38adc4ccb0a0b6d03d0bd907f5744a64c77ec3ebab74dc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:8c2de33ebbc32e8740f0a3502233a1e3f1fb047ea12feff6ed2dafe4d94d84d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127537940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e00a921b7d5673370fa7991a4ab42a344a3ea649274a23ca9a5a971ec38465`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:48 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:36:48 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:37:16 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 06 Mar 2021 07:37:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:37:16 GMT
USER kong
# Sat, 06 Mar 2021 07:37:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:37:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:37:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:37:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f56126da854435826e67895a0c0904e2d9192aec7b83e187b93fc9e34f9db19`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372cea5912641852de535666cf1cb0204d6ab7c67e54a5bf67440f91f0017f6c`  
		Last Modified: Sat, 06 Mar 2021 07:43:01 GMT  
		Size: 51.4 MB (51439924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4813e3fe68a31d3fbca2ea4ab673b0ae50dca5f95280bc9ce89670e2346b0b80`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-ubuntu`

```console
$ docker pull kong@sha256:f9110787d1f171565dc1cdd197bcaf9f530d975af0fbda1ade84237618b97cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:188f076744fb25cda43f7d8f4986d46036f2965119dbaef94d74913c0ad45357
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101037343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5f676a50f99644aa17ff23e363c2971513312fbd9e2a18738c9c97dbfd28f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:51:14 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:51:14 GMT
ARG KONG_VERSION=2.0.5
# Fri, 26 Mar 2021 07:51:14 GMT
ENV KONG_VERSION=2.0.5
# Fri, 26 Mar 2021 07:51:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Fri, 26 Mar 2021 07:51:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:51:31 GMT
USER kong
# Fri, 26 Mar 2021 07:51:32 GMT
RUN kong version
# Fri, 26 Mar 2021 07:51:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:51:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:51:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:51:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429915d3885ed85d706c71931d603adfd82a78a5da1a92d348dd04fe5732f0f6`  
		Last Modified: Fri, 26 Mar 2021 07:55:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac241621fc70a92aedec6716d5c8ad5b37803006284b20d06c77eaadd902a3ed`  
		Last Modified: Fri, 26 Mar 2021 07:55:30 GMT  
		Size: 55.1 MB (55072545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5121b270337f6503dfc3128c9bc4426f3f87f4b42fd603e9c3e78e268b4e9`  
		Last Modified: Fri, 26 Mar 2021 07:55:20 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e1b47c983877508b59221a602c5cc91bac8f22f11ff80ffc22d20167de94e3`  
		Last Modified: Fri, 26 Mar 2021 07:55:20 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2705e7dd0518af4a9c38edfd1092c04dbfbca05e3266383095e2e207ddfc1709
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93072709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47010f98eaabc4154f806c853cc83f2e95bb370fdfbe068b7e5e7cc58cfd7459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:35:48 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:35:49 GMT
ARG KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:35:50 GMT
ENV KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:36:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 21 Jan 2021 05:36:33 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:36:34 GMT
USER kong
# Thu, 21 Jan 2021 05:36:36 GMT
RUN kong version
# Thu, 21 Jan 2021 05:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:36:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:36:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:36:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e364343239094535f14c35ef5e131471b966188de44b93aeede0e05b1846721e`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0eac08498e298b622e08a7f87cd69a82817a5ace2acebed22998cd9e1b4fce`  
		Last Modified: Thu, 21 Jan 2021 05:39:00 GMT  
		Size: 52.2 MB (52185091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3d4450827002eb8ce5cfc3c6b803a2b4c617fb6dd4c9394aefd07a3c80ed0`  
		Last Modified: Thu, 21 Jan 2021 05:38:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858413272bc97018762df0a5c950702d25874f24c3830eb17215363a0e826b7`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5`

```console
$ docker pull kong@sha256:bbb13e25c34a5c4e96332d2b50eb3fcc32d7946a410b13d056ad905c9ec65325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5` - linux; amd64

```console
$ docker pull kong@sha256:cbd33d90779eb12eb7e613d8bdb8c4ab2007d307e8f50172b3673ff1a631fc0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52769878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e139591360b0b1a90c7ca74ee8284f71a1f0851b4a28f8d04135c4e64a51f8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:26:15 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:26:15 GMT
ARG KONG_VERSION=2.0.5
# Thu, 01 Apr 2021 14:26:15 GMT
ENV KONG_VERSION=2.0.5
# Thu, 01 Apr 2021 14:26:15 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Thu, 01 Apr 2021 14:26:16 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Thu, 01 Apr 2021 14:26:22 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Thu, 01 Apr 2021 14:26:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:23 GMT
USER kong
# Thu, 01 Apr 2021 14:26:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5615f2d578be1c601e3c8f7f5caa944e8b35a9dcccc414bbb4a83452f15f823`  
		Last Modified: Thu, 01 Apr 2021 14:28:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f6a30785898fddd810f8b06483b8b88ff2a52eb0524b873ebcae3086a6f270`  
		Last Modified: Thu, 01 Apr 2021 14:28:56 GMT  
		Size: 50.0 MB (49953667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3c1a6567c6914fd362c0b3d6800fd976c155e704650cc35d2c866df982bf88`  
		Last Modified: Thu, 01 Apr 2021 14:28:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-alpine`

```console
$ docker pull kong@sha256:bbb13e25c34a5c4e96332d2b50eb3fcc32d7946a410b13d056ad905c9ec65325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:cbd33d90779eb12eb7e613d8bdb8c4ab2007d307e8f50172b3673ff1a631fc0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52769878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e139591360b0b1a90c7ca74ee8284f71a1f0851b4a28f8d04135c4e64a51f8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:26:15 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:26:15 GMT
ARG KONG_VERSION=2.0.5
# Thu, 01 Apr 2021 14:26:15 GMT
ENV KONG_VERSION=2.0.5
# Thu, 01 Apr 2021 14:26:15 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Thu, 01 Apr 2021 14:26:16 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Thu, 01 Apr 2021 14:26:22 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Thu, 01 Apr 2021 14:26:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:23 GMT
USER kong
# Thu, 01 Apr 2021 14:26:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5615f2d578be1c601e3c8f7f5caa944e8b35a9dcccc414bbb4a83452f15f823`  
		Last Modified: Thu, 01 Apr 2021 14:28:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f6a30785898fddd810f8b06483b8b88ff2a52eb0524b873ebcae3086a6f270`  
		Last Modified: Thu, 01 Apr 2021 14:28:56 GMT  
		Size: 50.0 MB (49953667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3c1a6567c6914fd362c0b3d6800fd976c155e704650cc35d2c866df982bf88`  
		Last Modified: Thu, 01 Apr 2021 14:28:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-centos`

```console
$ docker pull kong@sha256:7a6ec5d8213e47be38adc4ccb0a0b6d03d0bd907f5744a64c77ec3ebab74dc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-centos` - linux; amd64

```console
$ docker pull kong@sha256:8c2de33ebbc32e8740f0a3502233a1e3f1fb047ea12feff6ed2dafe4d94d84d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127537940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e00a921b7d5673370fa7991a4ab42a344a3ea649274a23ca9a5a971ec38465`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:48 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:36:48 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:37:16 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 06 Mar 2021 07:37:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:37:16 GMT
USER kong
# Sat, 06 Mar 2021 07:37:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:37:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:37:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:37:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f56126da854435826e67895a0c0904e2d9192aec7b83e187b93fc9e34f9db19`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372cea5912641852de535666cf1cb0204d6ab7c67e54a5bf67440f91f0017f6c`  
		Last Modified: Sat, 06 Mar 2021 07:43:01 GMT  
		Size: 51.4 MB (51439924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4813e3fe68a31d3fbca2ea4ab673b0ae50dca5f95280bc9ce89670e2346b0b80`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-ubuntu`

```console
$ docker pull kong@sha256:f9110787d1f171565dc1cdd197bcaf9f530d975af0fbda1ade84237618b97cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:188f076744fb25cda43f7d8f4986d46036f2965119dbaef94d74913c0ad45357
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101037343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5f676a50f99644aa17ff23e363c2971513312fbd9e2a18738c9c97dbfd28f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:51:14 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:51:14 GMT
ARG KONG_VERSION=2.0.5
# Fri, 26 Mar 2021 07:51:14 GMT
ENV KONG_VERSION=2.0.5
# Fri, 26 Mar 2021 07:51:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Fri, 26 Mar 2021 07:51:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:51:31 GMT
USER kong
# Fri, 26 Mar 2021 07:51:32 GMT
RUN kong version
# Fri, 26 Mar 2021 07:51:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:51:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:51:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:51:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429915d3885ed85d706c71931d603adfd82a78a5da1a92d348dd04fe5732f0f6`  
		Last Modified: Fri, 26 Mar 2021 07:55:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac241621fc70a92aedec6716d5c8ad5b37803006284b20d06c77eaadd902a3ed`  
		Last Modified: Fri, 26 Mar 2021 07:55:30 GMT  
		Size: 55.1 MB (55072545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5121b270337f6503dfc3128c9bc4426f3f87f4b42fd603e9c3e78e268b4e9`  
		Last Modified: Fri, 26 Mar 2021 07:55:20 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e1b47c983877508b59221a602c5cc91bac8f22f11ff80ffc22d20167de94e3`  
		Last Modified: Fri, 26 Mar 2021 07:55:20 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2705e7dd0518af4a9c38edfd1092c04dbfbca05e3266383095e2e207ddfc1709
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93072709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47010f98eaabc4154f806c853cc83f2e95bb370fdfbe068b7e5e7cc58cfd7459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:35:48 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:35:49 GMT
ARG KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:35:50 GMT
ENV KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:36:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 21 Jan 2021 05:36:33 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:36:34 GMT
USER kong
# Thu, 21 Jan 2021 05:36:36 GMT
RUN kong version
# Thu, 21 Jan 2021 05:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:36:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:36:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:36:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e364343239094535f14c35ef5e131471b966188de44b93aeede0e05b1846721e`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0eac08498e298b622e08a7f87cd69a82817a5ace2acebed22998cd9e1b4fce`  
		Last Modified: Thu, 21 Jan 2021 05:39:00 GMT  
		Size: 52.2 MB (52185091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3d4450827002eb8ce5cfc3c6b803a2b4c617fb6dd4c9394aefd07a3c80ed0`  
		Last Modified: Thu, 21 Jan 2021 05:38:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858413272bc97018762df0a5c950702d25874f24c3830eb17215363a0e826b7`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1`

```console
$ docker pull kong@sha256:8bca78cf8872e3820237cde0c55f68a5fc4827019661b2696916b30e736d344f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1` - linux; amd64

```console
$ docker pull kong@sha256:1edd7f2d09ab55d2b798c78560fa15a4b103c272f5870a7519fcd86367dc37eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9c6a944c00a64698bea7c4d9bf7cd19ef43dd5727e9cf5c4867987ae5b6e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:56 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:25:57 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:26:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 14:26:05 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:05 GMT
USER kong
# Thu, 01 Apr 2021 14:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:05 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe2c7d38c835192e8413af7e2b8f9fd5d5683e8b1e1c1f8ed0521fc58fc3ad2`  
		Last Modified: Thu, 01 Apr 2021 14:28:29 GMT  
		Size: 50.3 MB (50339653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9718b42339b6ec02bbe8b2329d56d13d346ae0b28dd5a6b84d3fd7f9b9e9d9b`  
		Last Modified: Thu, 01 Apr 2021 14:28:20 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:03c60155bdc21a5799c5d63b2aed00f23e9879b57eef80fa5b4c44346486a751
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52668605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6e7f1a13d99efd9511d0a24385196beeb740be4794424bdc3aaa6f1a0ea67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:40:35 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:36 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 13:40:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:49 GMT
USER kong
# Thu, 01 Apr 2021 13:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:51 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a0a225641b64454a91f64ee061f2f954f4d868149027bbe1a3f2afc1bced6`  
		Last Modified: Thu, 01 Apr 2021 13:42:54 GMT  
		Size: 49.9 MB (49941870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb25f384af9ec44b1bfc0734445f8bb17a992cabc556a5be3a1e0a6603bb6fc`  
		Last Modified: Thu, 01 Apr 2021 13:42:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:8bca78cf8872e3820237cde0c55f68a5fc4827019661b2696916b30e736d344f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:1edd7f2d09ab55d2b798c78560fa15a4b103c272f5870a7519fcd86367dc37eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9c6a944c00a64698bea7c4d9bf7cd19ef43dd5727e9cf5c4867987ae5b6e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:56 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:25:57 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:26:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 14:26:05 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:05 GMT
USER kong
# Thu, 01 Apr 2021 14:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:05 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe2c7d38c835192e8413af7e2b8f9fd5d5683e8b1e1c1f8ed0521fc58fc3ad2`  
		Last Modified: Thu, 01 Apr 2021 14:28:29 GMT  
		Size: 50.3 MB (50339653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9718b42339b6ec02bbe8b2329d56d13d346ae0b28dd5a6b84d3fd7f9b9e9d9b`  
		Last Modified: Thu, 01 Apr 2021 14:28:20 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:03c60155bdc21a5799c5d63b2aed00f23e9879b57eef80fa5b4c44346486a751
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52668605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6e7f1a13d99efd9511d0a24385196beeb740be4794424bdc3aaa6f1a0ea67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:40:35 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:36 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 13:40:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:49 GMT
USER kong
# Thu, 01 Apr 2021 13:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:51 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a0a225641b64454a91f64ee061f2f954f4d868149027bbe1a3f2afc1bced6`  
		Last Modified: Thu, 01 Apr 2021 13:42:54 GMT  
		Size: 49.9 MB (49941870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb25f384af9ec44b1bfc0734445f8bb17a992cabc556a5be3a1e0a6603bb6fc`  
		Last Modified: Thu, 01 Apr 2021 13:42:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-centos`

```console
$ docker pull kong@sha256:77840b0da10999cf8e5f5fc40b74b9a529a4e2741bad37a4ec526ae15d3c54ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a9ffdeba8e9265dc75b4886b3c8f6331e6ceb4d9ca780e31b0cd540d98dc1a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127311261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcf1fde3c306e947cfc2a69e01e11d948b4be4b9890331393f37eaffc12bec1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:35:30 GMT
ARG KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:30 GMT
ENV KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:31 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 06 Mar 2021 07:36:02 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:36:02 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:03 GMT
USER kong
# Sat, 06 Mar 2021 07:36:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d58470d12b124664799e1a7498f5ab3c5c3c3e580293ff45e5d3b60b1705d4`  
		Last Modified: Sat, 06 Mar 2021 07:41:51 GMT  
		Size: 51.2 MB (51213243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8addfed624e6ff2dbb27909f1ac74b2b79dd7fec98a7bb7954075023ccfa583`  
		Last Modified: Sat, 06 Mar 2021 07:41:41 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-ubuntu`

```console
$ docker pull kong@sha256:2996a43ccd31eef4663ab675a796f0232e3af5171a910a33c2fe864b3094fc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5980a8a059ae11cb6db58faef722ad8f03556259598f9632012f3796cc32df53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0d7858cc558c8dc74aca701c77f2810f3cb8cedf4e93f82a553b969f57e2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:50:34 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:34 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:53 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:54 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:54 GMT
USER kong
# Fri, 26 Mar 2021 07:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:55 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3eb698e6d02079dc8282f61c17f743abcbdc0200517a88d1ee48be67432d58`  
		Last Modified: Fri, 26 Mar 2021 07:54:39 GMT  
		Size: 62.8 MB (62848061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c792b7a3ce2c394da24736e516c7d3f00ae35fe543bc80b60d4f71168ab806c`  
		Last Modified: Fri, 26 Mar 2021 07:54:28 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:49baf2f4e15be6f983e1c64447cac8320374e4febeecdb236d31baf651756995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125199807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1fde0c7a655bd82a5ce2e18ae7ffa4d9ed68905b1182906263de7418295374`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:34:29 GMT
ARG KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:34:30 GMT
ENV KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:35:34 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 05:35:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:35:38 GMT
USER kong
# Thu, 21 Jan 2021 05:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:35:39 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:35:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:35:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac4802aab8eabcd73e4641d6fe9c881be6b1d4564d4e3908ac28ae82444846f`  
		Last Modified: Thu, 21 Jan 2021 05:38:36 GMT  
		Size: 59.2 MB (59230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220a51772734a4fe75e8179450595e1682af3caec53ce05dd7891e8accb5811`  
		Last Modified: Thu, 21 Jan 2021 05:38:20 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4`

```console
$ docker pull kong@sha256:8bca78cf8872e3820237cde0c55f68a5fc4827019661b2696916b30e736d344f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4` - linux; amd64

```console
$ docker pull kong@sha256:1edd7f2d09ab55d2b798c78560fa15a4b103c272f5870a7519fcd86367dc37eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9c6a944c00a64698bea7c4d9bf7cd19ef43dd5727e9cf5c4867987ae5b6e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:56 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:25:57 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:26:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 14:26:05 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:05 GMT
USER kong
# Thu, 01 Apr 2021 14:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:05 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe2c7d38c835192e8413af7e2b8f9fd5d5683e8b1e1c1f8ed0521fc58fc3ad2`  
		Last Modified: Thu, 01 Apr 2021 14:28:29 GMT  
		Size: 50.3 MB (50339653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9718b42339b6ec02bbe8b2329d56d13d346ae0b28dd5a6b84d3fd7f9b9e9d9b`  
		Last Modified: Thu, 01 Apr 2021 14:28:20 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:03c60155bdc21a5799c5d63b2aed00f23e9879b57eef80fa5b4c44346486a751
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52668605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6e7f1a13d99efd9511d0a24385196beeb740be4794424bdc3aaa6f1a0ea67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:40:35 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:36 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 13:40:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:49 GMT
USER kong
# Thu, 01 Apr 2021 13:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:51 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a0a225641b64454a91f64ee061f2f954f4d868149027bbe1a3f2afc1bced6`  
		Last Modified: Thu, 01 Apr 2021 13:42:54 GMT  
		Size: 49.9 MB (49941870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb25f384af9ec44b1bfc0734445f8bb17a992cabc556a5be3a1e0a6603bb6fc`  
		Last Modified: Thu, 01 Apr 2021 13:42:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-alpine`

```console
$ docker pull kong@sha256:8bca78cf8872e3820237cde0c55f68a5fc4827019661b2696916b30e736d344f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:1edd7f2d09ab55d2b798c78560fa15a4b103c272f5870a7519fcd86367dc37eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9c6a944c00a64698bea7c4d9bf7cd19ef43dd5727e9cf5c4867987ae5b6e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:56 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:25:57 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 14:26:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 14:26:05 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:26:05 GMT
USER kong
# Thu, 01 Apr 2021 14:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:26:05 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:26:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:26:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe2c7d38c835192e8413af7e2b8f9fd5d5683e8b1e1c1f8ed0521fc58fc3ad2`  
		Last Modified: Thu, 01 Apr 2021 14:28:29 GMT  
		Size: 50.3 MB (50339653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9718b42339b6ec02bbe8b2329d56d13d346ae0b28dd5a6b84d3fd7f9b9e9d9b`  
		Last Modified: Thu, 01 Apr 2021 14:28:20 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:03c60155bdc21a5799c5d63b2aed00f23e9879b57eef80fa5b4c44346486a751
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52668605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6e7f1a13d99efd9511d0a24385196beeb740be4794424bdc3aaa6f1a0ea67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:40:35 GMT
ARG KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:36 GMT
ENV KONG_VERSION=2.1.4
# Thu, 01 Apr 2021 13:40:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 01 Apr 2021 13:40:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:49 GMT
USER kong
# Thu, 01 Apr 2021 13:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:51 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a0a225641b64454a91f64ee061f2f954f4d868149027bbe1a3f2afc1bced6`  
		Last Modified: Thu, 01 Apr 2021 13:42:54 GMT  
		Size: 49.9 MB (49941870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb25f384af9ec44b1bfc0734445f8bb17a992cabc556a5be3a1e0a6603bb6fc`  
		Last Modified: Thu, 01 Apr 2021 13:42:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-centos`

```console
$ docker pull kong@sha256:77840b0da10999cf8e5f5fc40b74b9a529a4e2741bad37a4ec526ae15d3c54ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a9ffdeba8e9265dc75b4886b3c8f6331e6ceb4d9ca780e31b0cd540d98dc1a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127311261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcf1fde3c306e947cfc2a69e01e11d948b4be4b9890331393f37eaffc12bec1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:35:30 GMT
ARG KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:30 GMT
ENV KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:31 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 06 Mar 2021 07:36:02 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:36:02 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:03 GMT
USER kong
# Sat, 06 Mar 2021 07:36:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d58470d12b124664799e1a7498f5ab3c5c3c3e580293ff45e5d3b60b1705d4`  
		Last Modified: Sat, 06 Mar 2021 07:41:51 GMT  
		Size: 51.2 MB (51213243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8addfed624e6ff2dbb27909f1ac74b2b79dd7fec98a7bb7954075023ccfa583`  
		Last Modified: Sat, 06 Mar 2021 07:41:41 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-ubuntu`

```console
$ docker pull kong@sha256:2996a43ccd31eef4663ab675a796f0232e3af5171a910a33c2fe864b3094fc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5980a8a059ae11cb6db58faef722ad8f03556259598f9632012f3796cc32df53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0d7858cc558c8dc74aca701c77f2810f3cb8cedf4e93f82a553b969f57e2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:50:34 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:34 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:53 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:54 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:54 GMT
USER kong
# Fri, 26 Mar 2021 07:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:55 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3eb698e6d02079dc8282f61c17f743abcbdc0200517a88d1ee48be67432d58`  
		Last Modified: Fri, 26 Mar 2021 07:54:39 GMT  
		Size: 62.8 MB (62848061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c792b7a3ce2c394da24736e516c7d3f00ae35fe543bc80b60d4f71168ab806c`  
		Last Modified: Fri, 26 Mar 2021 07:54:28 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:49baf2f4e15be6f983e1c64447cac8320374e4febeecdb236d31baf651756995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125199807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1fde0c7a655bd82a5ce2e18ae7ffa4d9ed68905b1182906263de7418295374`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:34:29 GMT
ARG KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:34:30 GMT
ENV KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:35:34 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 05:35:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:35:38 GMT
USER kong
# Thu, 21 Jan 2021 05:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:35:39 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:35:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:35:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac4802aab8eabcd73e4641d6fe9c881be6b1d4564d4e3908ac28ae82444846f`  
		Last Modified: Thu, 21 Jan 2021 05:38:36 GMT  
		Size: 59.2 MB (59230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220a51772734a4fe75e8179450595e1682af3caec53ce05dd7891e8accb5811`  
		Last Modified: Thu, 21 Jan 2021 05:38:20 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2`

```console
$ docker pull kong@sha256:90a2f0ef16df13728300dd32f7ef9d515c0c3fb6de530c89b3f95b4a287a89fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2` - linux; amd64

```console
$ docker pull kong@sha256:8d5245e99634f92bbdc573b6214c518cab3becf9e1b249ced095c1aae1c4d5b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d2e817ef089d93c8f57235d9e0f3db5d1d3a87905b32f0111c49d4bf0fab80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:38 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:38 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:47 GMT
USER kong
# Thu, 01 Apr 2021 14:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed255412c30bf74a7cb77660e06357daea643be9f2b5a23a87400556b85955c`  
		Last Modified: Thu, 01 Apr 2021 14:28:02 GMT  
		Size: 48.1 MB (48102729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144df33903e52dba5ab0cd47989d861e88f922684f61f0630a7fb8c1a789a45c`  
		Last Modified: Thu, 01 Apr 2021 14:27:54 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9d80ef701cd8e4d66867bf097f7a50480aae4ed112e243c33f18c3c22247387e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32146d0b0a33ed22a36327d38ade25d37c4f423b8f2acbf14765c54e4ad2a4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:58 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:01 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:02 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:03 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:13 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:40:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:16 GMT
USER kong
# Thu, 01 Apr 2021 13:40:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bfe3bda6511253fd3133d5904689073120f7bc7d52c26e5ddaa9593ce7af20`  
		Last Modified: Thu, 01 Apr 2021 13:42:19 GMT  
		Size: 47.7 MB (47712166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996770bd312187bb99c378b4466501f247aef0487dc64600d75fdb375dfbaf10`  
		Last Modified: Thu, 01 Apr 2021 13:42:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-alpine`

```console
$ docker pull kong@sha256:90a2f0ef16df13728300dd32f7ef9d515c0c3fb6de530c89b3f95b4a287a89fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8d5245e99634f92bbdc573b6214c518cab3becf9e1b249ced095c1aae1c4d5b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d2e817ef089d93c8f57235d9e0f3db5d1d3a87905b32f0111c49d4bf0fab80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:38 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:38 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:47 GMT
USER kong
# Thu, 01 Apr 2021 14:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed255412c30bf74a7cb77660e06357daea643be9f2b5a23a87400556b85955c`  
		Last Modified: Thu, 01 Apr 2021 14:28:02 GMT  
		Size: 48.1 MB (48102729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144df33903e52dba5ab0cd47989d861e88f922684f61f0630a7fb8c1a789a45c`  
		Last Modified: Thu, 01 Apr 2021 14:27:54 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9d80ef701cd8e4d66867bf097f7a50480aae4ed112e243c33f18c3c22247387e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32146d0b0a33ed22a36327d38ade25d37c4f423b8f2acbf14765c54e4ad2a4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:58 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:01 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:02 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:03 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:13 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:40:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:16 GMT
USER kong
# Thu, 01 Apr 2021 13:40:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bfe3bda6511253fd3133d5904689073120f7bc7d52c26e5ddaa9593ce7af20`  
		Last Modified: Thu, 01 Apr 2021 13:42:19 GMT  
		Size: 47.7 MB (47712166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996770bd312187bb99c378b4466501f247aef0487dc64600d75fdb375dfbaf10`  
		Last Modified: Thu, 01 Apr 2021 13:42:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-centos`

```console
$ docker pull kong@sha256:b870aaccdc0455456d5eca3f954663d8132f719c18fa2d47ee4c38673bda0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:b99fd6ff86818d05cee82ce71a63bdfb661693c622b27193b96750dffd562829
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127429787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f71964a13e0b5e7c5d00426038b3ddc6fd2054f7036cee00dd53c7503fe848`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ENV KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
# Sat, 06 Mar 2021 07:34:44 GMT
# ARGS: KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:34:44 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:34:44 GMT
USER kong
# Sat, 06 Mar 2021 07:34:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:34:45 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:34:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:34:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec7fea4bc2c9f42b92666a7ede8cf5320bad3f3056c09c33312e1b0d3b948d`  
		Last Modified: Sat, 06 Mar 2021 07:40:40 GMT  
		Size: 51.3 MB (51331768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097cf65a24bc9245c0d8fb506e5c58d9b0060bcefc75df330ae0581f5e0f76b1`  
		Last Modified: Sat, 06 Mar 2021 07:40:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-ubuntu`

```console
$ docker pull kong@sha256:d2b356e70f1422567ea71ba2c3c8b0c3c9e666625589875d7a744edeaa4456f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:633f9725bbb07c54a82dedf2b085e6918ae968e3f8244c8f1f900df7e971fb8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133978267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f5fea5d432a10856a87964116d1dce39dc21c2e2720616aec3f6444e8bfb2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:49:55 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:55 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:50:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:16 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:16 GMT
USER kong
# Fri, 26 Mar 2021 07:50:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:16 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acffd89d236b04f1fc078cc30b74c04a573e16e9430fe4badd7ee208106dad7`  
		Last Modified: Fri, 26 Mar 2021 07:53:53 GMT  
		Size: 62.9 MB (62931733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa38b78d1f6ce40f8dca1891c9a5e4122228c4764d64e7d450dca06a7d9a16a5`  
		Last Modified: Fri, 26 Mar 2021 07:53:42 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6c23c408a685f6ea1a5d4147c37672d50bfd0cad13db46cf3eb668f329cf9f67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125313399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7aae149cd0de107495cf4ec47a1de269c1f3cf1feb61c4cf816dfc52304ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Mar 2021 01:06:13 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:06:14 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:07:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Tue, 02 Mar 2021 01:07:35 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:07:36 GMT
USER kong
# Tue, 02 Mar 2021 01:07:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:07:37 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:07:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:07:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe89e14a980b1beac708e2a9316b0a92318359dc549fea9705c13c9975d101`  
		Last Modified: Tue, 02 Mar 2021 01:09:21 GMT  
		Size: 59.3 MB (59344049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb25e8d274e645369666fb60d5a19c9ad4fcf8970d03f7a468339c980c10c47`  
		Last Modified: Tue, 02 Mar 2021 01:09:02 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2`

```console
$ docker pull kong@sha256:90a2f0ef16df13728300dd32f7ef9d515c0c3fb6de530c89b3f95b4a287a89fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2` - linux; amd64

```console
$ docker pull kong@sha256:8d5245e99634f92bbdc573b6214c518cab3becf9e1b249ced095c1aae1c4d5b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d2e817ef089d93c8f57235d9e0f3db5d1d3a87905b32f0111c49d4bf0fab80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:38 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:38 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:47 GMT
USER kong
# Thu, 01 Apr 2021 14:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed255412c30bf74a7cb77660e06357daea643be9f2b5a23a87400556b85955c`  
		Last Modified: Thu, 01 Apr 2021 14:28:02 GMT  
		Size: 48.1 MB (48102729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144df33903e52dba5ab0cd47989d861e88f922684f61f0630a7fb8c1a789a45c`  
		Last Modified: Thu, 01 Apr 2021 14:27:54 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9d80ef701cd8e4d66867bf097f7a50480aae4ed112e243c33f18c3c22247387e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32146d0b0a33ed22a36327d38ade25d37c4f423b8f2acbf14765c54e4ad2a4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:58 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:01 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:02 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:03 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:13 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:40:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:16 GMT
USER kong
# Thu, 01 Apr 2021 13:40:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bfe3bda6511253fd3133d5904689073120f7bc7d52c26e5ddaa9593ce7af20`  
		Last Modified: Thu, 01 Apr 2021 13:42:19 GMT  
		Size: 47.7 MB (47712166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996770bd312187bb99c378b4466501f247aef0487dc64600d75fdb375dfbaf10`  
		Last Modified: Thu, 01 Apr 2021 13:42:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-alpine`

```console
$ docker pull kong@sha256:90a2f0ef16df13728300dd32f7ef9d515c0c3fb6de530c89b3f95b4a287a89fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8d5245e99634f92bbdc573b6214c518cab3becf9e1b249ced095c1aae1c4d5b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d2e817ef089d93c8f57235d9e0f3db5d1d3a87905b32f0111c49d4bf0fab80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:38 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:38 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 14:25:39 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:39 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 14:25:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:47 GMT
USER kong
# Thu, 01 Apr 2021 14:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed255412c30bf74a7cb77660e06357daea643be9f2b5a23a87400556b85955c`  
		Last Modified: Thu, 01 Apr 2021 14:28:02 GMT  
		Size: 48.1 MB (48102729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144df33903e52dba5ab0cd47989d861e88f922684f61f0630a7fb8c1a789a45c`  
		Last Modified: Thu, 01 Apr 2021 14:27:54 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9d80ef701cd8e4d66867bf097f7a50480aae4ed112e243c33f18c3c22247387e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32146d0b0a33ed22a36327d38ade25d37c4f423b8f2acbf14765c54e4ad2a4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:58 GMT
ARG KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ENV KONG_VERSION=2.2.2
# Thu, 01 Apr 2021 13:39:59 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:01 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Thu, 01 Apr 2021 13:40:02 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:03 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Thu, 01 Apr 2021 13:40:13 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:40:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:40:16 GMT
USER kong
# Thu, 01 Apr 2021 13:40:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:40:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:40:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bfe3bda6511253fd3133d5904689073120f7bc7d52c26e5ddaa9593ce7af20`  
		Last Modified: Thu, 01 Apr 2021 13:42:19 GMT  
		Size: 47.7 MB (47712166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996770bd312187bb99c378b4466501f247aef0487dc64600d75fdb375dfbaf10`  
		Last Modified: Thu, 01 Apr 2021 13:42:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-centos`

```console
$ docker pull kong@sha256:b870aaccdc0455456d5eca3f954663d8132f719c18fa2d47ee4c38673bda0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:b99fd6ff86818d05cee82ce71a63bdfb661693c622b27193b96750dffd562829
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127429787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f71964a13e0b5e7c5d00426038b3ddc6fd2054f7036cee00dd53c7503fe848`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ENV KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
# Sat, 06 Mar 2021 07:34:44 GMT
# ARGS: KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:34:44 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:34:44 GMT
USER kong
# Sat, 06 Mar 2021 07:34:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:34:45 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:34:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:34:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec7fea4bc2c9f42b92666a7ede8cf5320bad3f3056c09c33312e1b0d3b948d`  
		Last Modified: Sat, 06 Mar 2021 07:40:40 GMT  
		Size: 51.3 MB (51331768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097cf65a24bc9245c0d8fb506e5c58d9b0060bcefc75df330ae0581f5e0f76b1`  
		Last Modified: Sat, 06 Mar 2021 07:40:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-ubuntu`

```console
$ docker pull kong@sha256:d2b356e70f1422567ea71ba2c3c8b0c3c9e666625589875d7a744edeaa4456f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:633f9725bbb07c54a82dedf2b085e6918ae968e3f8244c8f1f900df7e971fb8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133978267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f5fea5d432a10856a87964116d1dce39dc21c2e2720616aec3f6444e8bfb2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:49:55 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:55 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:50:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:16 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:16 GMT
USER kong
# Fri, 26 Mar 2021 07:50:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:16 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acffd89d236b04f1fc078cc30b74c04a573e16e9430fe4badd7ee208106dad7`  
		Last Modified: Fri, 26 Mar 2021 07:53:53 GMT  
		Size: 62.9 MB (62931733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa38b78d1f6ce40f8dca1891c9a5e4122228c4764d64e7d450dca06a7d9a16a5`  
		Last Modified: Fri, 26 Mar 2021 07:53:42 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6c23c408a685f6ea1a5d4147c37672d50bfd0cad13db46cf3eb668f329cf9f67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125313399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7aae149cd0de107495cf4ec47a1de269c1f3cf1feb61c4cf816dfc52304ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Mar 2021 01:06:13 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:06:14 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:07:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Tue, 02 Mar 2021 01:07:35 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:07:36 GMT
USER kong
# Tue, 02 Mar 2021 01:07:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:07:37 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:07:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:07:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe89e14a980b1beac708e2a9316b0a92318359dc549fea9705c13c9975d101`  
		Last Modified: Tue, 02 Mar 2021 01:09:21 GMT  
		Size: 59.3 MB (59344049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb25e8d274e645369666fb60d5a19c9ad4fcf8970d03f7a468339c980c10c47`  
		Last Modified: Tue, 02 Mar 2021 01:09:02 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-alpine`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-centos`

```console
$ docker pull kong@sha256:63c7a5459162f96670d69397815c3cf7966f5c4cc65feaafe07051a72e6d2da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.3-centos` - linux; amd64

```console
$ docker pull kong@sha256:7d88eecef23471ad76522ea6be93c56e9ae83de5521ddb7ecd35b9cde89bfb89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127461132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f887f3447b92aa427c43a6c8d6c128cdded951a2d6c5c5d19d441e8b863ea8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
# Sat, 06 Mar 2021 07:32:57 GMT
# ARGS: KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:32:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:32:58 GMT
USER kong
# Sat, 06 Mar 2021 07:32:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:32:59 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:32:59 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:32:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bab90e7db9fd0876a6c6ee71dff10e19542928163fd63e82acecb4f9d497a1c`  
		Last Modified: Sat, 06 Mar 2021 07:39:27 GMT  
		Size: 51.4 MB (51363113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdaad95bf8bd054cd1f7cda0a7b056bde84001412bfde25b58c0811768988ff`  
		Last Modified: Sat, 06 Mar 2021 07:39:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-ubuntu`

```console
$ docker pull kong@sha256:a7722ab924713f2dde2dd2f12c26b5e99e9fc040c2753ef7d3a747575903cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:04e830cc5adbbfb8e410ec41a12454718130286c852ba404b2db483cc6c1cbd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3547c5f087a61cfde7927c87c52a4c5d071419dea63f34506bc8f0dffa095dce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:48:31 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:31 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:49:36 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:49:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:37 GMT
USER kong
# Fri, 26 Mar 2021 07:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164fd2e347006e7ea5368a6c544a851ff1023b68f35f01273e4ba5ff69377b3`  
		Last Modified: Fri, 26 Mar 2021 07:53:04 GMT  
		Size: 63.0 MB (62965553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69b3edcd0e49b2e0fbd0d8fe23549b38d01dcb805d5bd9506133aaecacf86ed`  
		Last Modified: Fri, 26 Mar 2021 07:52:53 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:74f104a8dea77d1504c12ed59a6dbcade78b9810477072df77c566c73258a944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125351993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fadd75ad516e36f3733cb8aa8b1234aa7fe4428fbfec68f629a559549d1eee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 06 Mar 2021 01:43:23 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:43:24 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:44:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 06 Mar 2021 01:44:18 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:44:19 GMT
USER kong
# Sat, 06 Mar 2021 01:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:44:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:44:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:44:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6a000ab4c5dba26b3a2a9b2ff40ad15c5bd087547d4ead387e544dd4994fb`  
		Last Modified: Sat, 06 Mar 2021 01:45:56 GMT  
		Size: 59.4 MB (59382644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de241f277a6749a12c8e5e7be3a45d232043c0249227796c146b22f18249833`  
		Last Modified: Sat, 06 Mar 2021 01:45:40 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-alpine`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-centos`

```console
$ docker pull kong@sha256:63c7a5459162f96670d69397815c3cf7966f5c4cc65feaafe07051a72e6d2da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.3.3-centos` - linux; amd64

```console
$ docker pull kong@sha256:7d88eecef23471ad76522ea6be93c56e9ae83de5521ddb7ecd35b9cde89bfb89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127461132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f887f3447b92aa427c43a6c8d6c128cdded951a2d6c5c5d19d441e8b863ea8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
# Sat, 06 Mar 2021 07:32:57 GMT
# ARGS: KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:32:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:32:58 GMT
USER kong
# Sat, 06 Mar 2021 07:32:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:32:59 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:32:59 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:32:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bab90e7db9fd0876a6c6ee71dff10e19542928163fd63e82acecb4f9d497a1c`  
		Last Modified: Sat, 06 Mar 2021 07:39:27 GMT  
		Size: 51.4 MB (51363113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdaad95bf8bd054cd1f7cda0a7b056bde84001412bfde25b58c0811768988ff`  
		Last Modified: Sat, 06 Mar 2021 07:39:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-ubuntu`

```console
$ docker pull kong@sha256:a7722ab924713f2dde2dd2f12c26b5e99e9fc040c2753ef7d3a747575903cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:04e830cc5adbbfb8e410ec41a12454718130286c852ba404b2db483cc6c1cbd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3547c5f087a61cfde7927c87c52a4c5d071419dea63f34506bc8f0dffa095dce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:48:31 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:31 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:49:36 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:49:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:37 GMT
USER kong
# Fri, 26 Mar 2021 07:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164fd2e347006e7ea5368a6c544a851ff1023b68f35f01273e4ba5ff69377b3`  
		Last Modified: Fri, 26 Mar 2021 07:53:04 GMT  
		Size: 63.0 MB (62965553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69b3edcd0e49b2e0fbd0d8fe23549b38d01dcb805d5bd9506133aaecacf86ed`  
		Last Modified: Fri, 26 Mar 2021 07:52:53 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:74f104a8dea77d1504c12ed59a6dbcade78b9810477072df77c566c73258a944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125351993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fadd75ad516e36f3733cb8aa8b1234aa7fe4428fbfec68f629a559549d1eee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 06 Mar 2021 01:43:23 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:43:24 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:44:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 06 Mar 2021 01:44:18 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:44:19 GMT
USER kong
# Sat, 06 Mar 2021 01:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:44:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:44:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:44:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6a000ab4c5dba26b3a2a9b2ff40ad15c5bd087547d4ead387e544dd4994fb`  
		Last Modified: Sat, 06 Mar 2021 01:45:56 GMT  
		Size: 59.4 MB (59382644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de241f277a6749a12c8e5e7be3a45d232043c0249227796c146b22f18249833`  
		Last Modified: Sat, 06 Mar 2021 01:45:40 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:63c7a5459162f96670d69397815c3cf7966f5c4cc65feaafe07051a72e6d2da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:7d88eecef23471ad76522ea6be93c56e9ae83de5521ddb7ecd35b9cde89bfb89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127461132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f887f3447b92aa427c43a6c8d6c128cdded951a2d6c5c5d19d441e8b863ea8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
# Sat, 06 Mar 2021 07:32:57 GMT
# ARGS: KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:32:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:32:58 GMT
USER kong
# Sat, 06 Mar 2021 07:32:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:32:59 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:32:59 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:32:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bab90e7db9fd0876a6c6ee71dff10e19542928163fd63e82acecb4f9d497a1c`  
		Last Modified: Sat, 06 Mar 2021 07:39:27 GMT  
		Size: 51.4 MB (51363113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdaad95bf8bd054cd1f7cda0a7b056bde84001412bfde25b58c0811768988ff`  
		Last Modified: Sat, 06 Mar 2021 07:39:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:dbc366a3c360243c5a3667738458e4fadf3cb4fa854c5e2f5aa1a412ce1bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:8cc07093bc19e2bcbf078b579165aa93416cae192ff92b902351ab4aa20718c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80622064f4858c37e944be6839acce6659e7b4f05081feeb90e9779134b59da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 14:25:19 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 14:25:19 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 14:25:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 14:25:20 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:20 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 14:25:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 14:25:28 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 14:25:29 GMT
USER kong
# Thu, 01 Apr 2021 14:25:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:25:29 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 14:25:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 14:25:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e7990a1a1335d39899edc2938b412decd1e592caf057d18ab0226367d3e4da`  
		Last Modified: Thu, 01 Apr 2021 14:27:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c731d1e15d416476a977415f6621ffb5dd1e8bfe7d4d605d059d503d63e030`  
		Last Modified: Thu, 01 Apr 2021 14:27:19 GMT  
		Size: 48.1 MB (48136743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b134474814201e6b9e2de7e66518f51da2e8f8b8c50fe5149c443b9f477999f`  
		Last Modified: Thu, 01 Apr 2021 14:27:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8baef1499c836a5ead7cc313d644345288268814b399cb3c090aa0dde7157e42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50474917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216112af0ba6ba50e70f28a3ee5ff501cde49429852d0f555344afbb48a365b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:39:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 01 Apr 2021 13:39:22 GMT
ARG ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ENV ASSET=ce
# Thu, 01 Apr 2021 13:39:23 GMT
ARG EE_PORTS
# Thu, 01 Apr 2021 13:39:24 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 01 Apr 2021 13:39:25 GMT
ARG KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ENV KONG_VERSION=2.3.3
# Thu, 01 Apr 2021 13:39:26 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Thu, 01 Apr 2021 13:39:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:29 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Thu, 01 Apr 2021 13:39:40 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 01 Apr 2021 13:39:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:39:43 GMT
USER kong
# Thu, 01 Apr 2021 13:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:39:44 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Apr 2021 13:39:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 13:39:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d662de68ef79de2102c7d691f0bb8460e07f4a80512f0e5c52df2db9e20f8e8`  
		Last Modified: Thu, 01 Apr 2021 13:41:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800ac016936c6e32cd04afc15191ce1233c8fe5e976a57747e4e8d5b8db8b5a`  
		Last Modified: Thu, 01 Apr 2021 13:41:46 GMT  
		Size: 47.7 MB (47748181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07581418082abae0fc5003a3f36bfb7bc4466b474e066da8cd565723676e2596`  
		Last Modified: Thu, 01 Apr 2021 13:41:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:a7722ab924713f2dde2dd2f12c26b5e99e9fc040c2753ef7d3a747575903cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:04e830cc5adbbfb8e410ec41a12454718130286c852ba404b2db483cc6c1cbd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3547c5f087a61cfde7927c87c52a4c5d071419dea63f34506bc8f0dffa095dce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:48:31 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:31 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:49:36 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:49:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:37 GMT
USER kong
# Fri, 26 Mar 2021 07:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164fd2e347006e7ea5368a6c544a851ff1023b68f35f01273e4ba5ff69377b3`  
		Last Modified: Fri, 26 Mar 2021 07:53:04 GMT  
		Size: 63.0 MB (62965553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69b3edcd0e49b2e0fbd0d8fe23549b38d01dcb805d5bd9506133aaecacf86ed`  
		Last Modified: Fri, 26 Mar 2021 07:52:53 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:74f104a8dea77d1504c12ed59a6dbcade78b9810477072df77c566c73258a944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125351993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fadd75ad516e36f3733cb8aa8b1234aa7fe4428fbfec68f629a559549d1eee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 06 Mar 2021 01:43:23 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:43:24 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:44:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 06 Mar 2021 01:44:18 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:44:19 GMT
USER kong
# Sat, 06 Mar 2021 01:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:44:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:44:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:44:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6a000ab4c5dba26b3a2a9b2ff40ad15c5bd087547d4ead387e544dd4994fb`  
		Last Modified: Sat, 06 Mar 2021 01:45:56 GMT  
		Size: 59.4 MB (59382644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de241f277a6749a12c8e5e7be3a45d232043c0249227796c146b22f18249833`  
		Last Modified: Sat, 06 Mar 2021 01:45:40 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
