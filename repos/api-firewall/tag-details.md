<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.7`](#api-firewall067)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.7`

```console
$ docker pull api-firewall@sha256:d9ef0a36337f00a6e6f3fa4b3990a2a6fdcdfc9fc44508281957efb4028f9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `api-firewall:0.6.7` - linux; amd64

```console
$ docker pull api-firewall@sha256:eb916dab11928d8fdf8207c2e7d8a936a70055e219d9e92807315fb4c4380ba9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3918e571c2ab2f2834d5656c6abd2ca1d213db1865d53c723d99cd03b5ea87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:00:47 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 05 Apr 2022 04:00:47 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 04:00:48 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 05 Apr 2022 04:00:48 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Tue, 05 Apr 2022 04:00:49 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 05 Apr 2022 04:00:50 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 05 Apr 2022 04:00:50 GMT
USER api-firewall
# Tue, 05 Apr 2022 04:00:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 04:00:50 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34205ad7e15a85fb6238ca662f347b83dd42d9181af0d2bb10ca0df5c7ee203`  
		Last Modified: Tue, 05 Apr 2022 04:00:59 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8295e4bd78d624e69424aabdbfc43632725092ac4fe96fa403977805bd8f768b`  
		Last Modified: Tue, 05 Apr 2022 04:01:00 GMT  
		Size: 4.7 MB (4675176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26856ec8c7575727c2684f995b99bf4c6096f37f8e7e9b420d579051583f905`  
		Last Modified: Tue, 05 Apr 2022 04:00:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.7` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:de3872cfdd407c0ce62254dcabedb24375ec3691febeafc08dccf21340696c2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7104195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7865720904f1ef9a7f3da5a1f602d62741869657c8cb1aaccd2bdda24f4df42e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:36:28 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 05 Apr 2022 07:36:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:36:30 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 05 Apr 2022 07:36:31 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Tue, 05 Apr 2022 07:36:33 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 05 Apr 2022 07:36:35 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 05 Apr 2022 07:36:35 GMT
USER api-firewall
# Tue, 05 Apr 2022 07:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:36:37 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dfcd6871e1e354662d6653b214f845c3e889d8c19e9a5fcad07ca5739ffcf4`  
		Last Modified: Tue, 05 Apr 2022 07:36:50 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1268ae58b7cc2e3ec9aa1f1d0444568fb1f0a343fda79575ecfbf071550affb1`  
		Last Modified: Tue, 05 Apr 2022 07:36:51 GMT  
		Size: 4.4 MB (4386162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e492d0f5a84173caa7ccc0dcd078833f92ae6e442d6a2b8d91defc7ff09725db`  
		Last Modified: Tue, 05 Apr 2022 07:36:50 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d9ef0a36337f00a6e6f3fa4b3990a2a6fdcdfc9fc44508281957efb4028f9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:eb916dab11928d8fdf8207c2e7d8a936a70055e219d9e92807315fb4c4380ba9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3918e571c2ab2f2834d5656c6abd2ca1d213db1865d53c723d99cd03b5ea87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:00:47 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 05 Apr 2022 04:00:47 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 04:00:48 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 05 Apr 2022 04:00:48 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Tue, 05 Apr 2022 04:00:49 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 05 Apr 2022 04:00:50 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 05 Apr 2022 04:00:50 GMT
USER api-firewall
# Tue, 05 Apr 2022 04:00:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 04:00:50 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34205ad7e15a85fb6238ca662f347b83dd42d9181af0d2bb10ca0df5c7ee203`  
		Last Modified: Tue, 05 Apr 2022 04:00:59 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8295e4bd78d624e69424aabdbfc43632725092ac4fe96fa403977805bd8f768b`  
		Last Modified: Tue, 05 Apr 2022 04:01:00 GMT  
		Size: 4.7 MB (4675176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26856ec8c7575727c2684f995b99bf4c6096f37f8e7e9b420d579051583f905`  
		Last Modified: Tue, 05 Apr 2022 04:00:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:de3872cfdd407c0ce62254dcabedb24375ec3691febeafc08dccf21340696c2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7104195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7865720904f1ef9a7f3da5a1f602d62741869657c8cb1aaccd2bdda24f4df42e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:36:28 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 05 Apr 2022 07:36:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:36:30 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 05 Apr 2022 07:36:31 GMT
ENV APIFIREWALL_VERSION=v0.6.7
# Tue, 05 Apr 2022 07:36:33 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb61a3ca620340a76f97856ec30190de8422535c31d17ddc89019e87825d60b9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='cdcd6679536e3e0fa0d5cdd8f422ef58f31f65c2d279228150c269c32641dd1d';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='0850d87b52624085265554605f46df5cda2a006d7b9dc9a7d369cdb9c9c88305';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 05 Apr 2022 07:36:35 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 05 Apr 2022 07:36:35 GMT
USER api-firewall
# Tue, 05 Apr 2022 07:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:36:37 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dfcd6871e1e354662d6653b214f845c3e889d8c19e9a5fcad07ca5739ffcf4`  
		Last Modified: Tue, 05 Apr 2022 07:36:50 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1268ae58b7cc2e3ec9aa1f1d0444568fb1f0a343fda79575ecfbf071550affb1`  
		Last Modified: Tue, 05 Apr 2022 07:36:51 GMT  
		Size: 4.4 MB (4386162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e492d0f5a84173caa7ccc0dcd078833f92ae6e442d6a2b8d91defc7ff09725db`  
		Last Modified: Tue, 05 Apr 2022 07:36:50 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
