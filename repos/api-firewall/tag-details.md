<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.7`](#api-firewall067)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.7`

```console
$ docker pull api-firewall@sha256:e71689a39137db9e45731bf830e3f435831640f82557168e9ec4ffaf549a49fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `api-firewall:0.6.7` - linux; amd64

```console
$ docker pull api-firewall@sha256:3200b56ebb04fa776d1b7e0f608fb86d225b69bbd34393fad450bca4aa399d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c417b88f871432846e05b811f5512166c004ab36ebfe7fc7eb62f4fc028add3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:07:15 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 17 Mar 2022 08:07:15 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 08:07:16 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 17 Mar 2022 08:07:16 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Thu, 17 Mar 2022 08:07:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 17 Mar 2022 08:07:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 17 Mar 2022 08:07:19 GMT
USER api-firewall
# Thu, 17 Mar 2022 08:07:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 08:07:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093f11fb3b4646e7359b04d9885c906a9a04de212f60f42bfbd91502cb27b139`  
		Last Modified: Thu, 17 Mar 2022 08:07:27 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa05880e4a31ba716c32c71f7be8aa6d39b2452050c977eade14076685febca8`  
		Last Modified: Thu, 17 Mar 2022 08:07:28 GMT  
		Size: 4.7 MB (4675159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da351d03bb78e059d31a93cc693c1ea3ed66fa0f033c8af0ba12fe556db881c6`  
		Last Modified: Thu, 17 Mar 2022 08:07:27 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.7` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:8a81cda917613c3f439dfa49d0792ec97dae1353d9566f8eb9d06e1ef296f547
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005bcf3ab2bbbdf25db25bbde827486bb5ad409482d43184a787665bc2c31ecc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 06:07:53 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 17 Mar 2022 06:07:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 06:07:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 17 Mar 2022 06:07:56 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Thu, 17 Mar 2022 06:07:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 17 Mar 2022 06:08:00 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 17 Mar 2022 06:08:00 GMT
USER api-firewall
# Thu, 17 Mar 2022 06:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 06:08:02 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6327a4b665ffc290376b84f773ca30c6aa6b7dfd362f294c38447f7ccb02b337`  
		Last Modified: Thu, 17 Mar 2022 06:08:16 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c425e15544d276e664cc899357a02e354d4f9d500b74e0edf11e6fa6b9325792`  
		Last Modified: Thu, 17 Mar 2022 06:08:16 GMT  
		Size: 4.4 MB (4386117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73abf77a6d8c34d6c1ab960aba3e8622cf600af0eddab29117814cf617fc59`  
		Last Modified: Thu, 17 Mar 2022 06:08:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:e71689a39137db9e45731bf830e3f435831640f82557168e9ec4ffaf549a49fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:3200b56ebb04fa776d1b7e0f608fb86d225b69bbd34393fad450bca4aa399d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c417b88f871432846e05b811f5512166c004ab36ebfe7fc7eb62f4fc028add3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:07:15 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 17 Mar 2022 08:07:15 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 08:07:16 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 17 Mar 2022 08:07:16 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Thu, 17 Mar 2022 08:07:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 17 Mar 2022 08:07:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 17 Mar 2022 08:07:19 GMT
USER api-firewall
# Thu, 17 Mar 2022 08:07:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 08:07:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093f11fb3b4646e7359b04d9885c906a9a04de212f60f42bfbd91502cb27b139`  
		Last Modified: Thu, 17 Mar 2022 08:07:27 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa05880e4a31ba716c32c71f7be8aa6d39b2452050c977eade14076685febca8`  
		Last Modified: Thu, 17 Mar 2022 08:07:28 GMT  
		Size: 4.7 MB (4675159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da351d03bb78e059d31a93cc693c1ea3ed66fa0f033c8af0ba12fe556db881c6`  
		Last Modified: Thu, 17 Mar 2022 08:07:27 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:8a81cda917613c3f439dfa49d0792ec97dae1353d9566f8eb9d06e1ef296f547
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005bcf3ab2bbbdf25db25bbde827486bb5ad409482d43184a787665bc2c31ecc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 06:07:53 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 17 Mar 2022 06:07:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 06:07:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 17 Mar 2022 06:07:56 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Thu, 17 Mar 2022 06:07:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 17 Mar 2022 06:08:00 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 17 Mar 2022 06:08:00 GMT
USER api-firewall
# Thu, 17 Mar 2022 06:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 06:08:02 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6327a4b665ffc290376b84f773ca30c6aa6b7dfd362f294c38447f7ccb02b337`  
		Last Modified: Thu, 17 Mar 2022 06:08:16 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c425e15544d276e664cc899357a02e354d4f9d500b74e0edf11e6fa6b9325792`  
		Last Modified: Thu, 17 Mar 2022 06:08:16 GMT  
		Size: 4.4 MB (4386117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73abf77a6d8c34d6c1ab960aba3e8622cf600af0eddab29117814cf617fc59`  
		Last Modified: Thu, 17 Mar 2022 06:08:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
