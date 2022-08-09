<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.8`](#api-firewall068)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.8`

```console
$ docker pull api-firewall@sha256:b540611885ccd5b45cec43f3816ee441d6fbe9ea05bb54f8a50351303dffb2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.8` - linux; amd64

```console
$ docker pull api-firewall@sha256:c2ddf78dead8053c2fc2934c8596e081ac575a6f0fdd35f4824703681e3728f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7579923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2557517f85256294702dafbd88e3fb62c567277548bffe6ff868eb4ba657a36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:47:39 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 09 Aug 2022 17:47:39 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 17:47:39 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 09 Aug 2022 17:47:39 GMT
ENV APIFIREWALL_VERSION=v0.6.8
# Tue, 09 Aug 2022 17:47:41 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='af8e49e7ebf19d68b4dcf09a0f0b04b36a5c6e3f556549cb48852fcebac03892';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b15fa8bfb98d23760eac894002db79420cdc321c1f1baabf60fba54556dfdab7';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='d37c9cef562788caf0177224516c555808251a6d79a368b4902424d57037d023';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 09 Aug 2022 17:47:41 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 09 Aug 2022 17:47:41 GMT
USER api-firewall
# Tue, 09 Aug 2022 17:47:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 17:47:41 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e62924cbb5cae95f3719d409db2c9d3db9b2566cefe562b49879111b3c78b66`  
		Last Modified: Tue, 09 Aug 2022 17:47:49 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a238989c27ee4f9089df52b4f5af75ea74f4fae1d6a8d1586008974d67787`  
		Last Modified: Tue, 09 Aug 2022 17:47:50 GMT  
		Size: 4.8 MB (4754859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f619bbb80421d4f9885e17d2514dce73fb8adcd9dfc1aaec17f007a71dba1b`  
		Last Modified: Tue, 09 Aug 2022 17:47:49 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.8` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:ed0536610a9bbd163670ba0ad1ac4861705c0dbba724bedfe3dca8030fb7d3f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142522584cde6b75be3387a1ecd9d783050d295db84bf7e5c668aa64eb4d6fa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:56:18 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Jul 2022 22:56:19 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 22:56:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 19 Jul 2022 22:56:21 GMT
ENV APIFIREWALL_VERSION=v0.6.8
# Tue, 19 Jul 2022 22:56:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='af8e49e7ebf19d68b4dcf09a0f0b04b36a5c6e3f556549cb48852fcebac03892';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b15fa8bfb98d23760eac894002db79420cdc321c1f1baabf60fba54556dfdab7';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='d37c9cef562788caf0177224516c555808251a6d79a368b4902424d57037d023';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 19 Jul 2022 22:56:25 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 19 Jul 2022 22:56:25 GMT
USER api-firewall
# Tue, 19 Jul 2022 22:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 22:56:27 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dc8c65823421c8e5e29a6df3db37e534afb9f770dada80c22998c3595d7861`  
		Last Modified: Tue, 19 Jul 2022 22:56:40 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801b25042915e7ee577900b032e35a3158baf90dca58e59044ff040948a4c3a8`  
		Last Modified: Tue, 19 Jul 2022 22:56:41 GMT  
		Size: 4.5 MB (4460213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68464705dd22e8f9d0d2941db944bf97defa5f48dc63db331de5d196c191747`  
		Last Modified: Tue, 19 Jul 2022 22:56:41 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.8` - linux; 386

```console
$ docker pull api-firewall@sha256:1018c58d71d209d919edbefe6067b4797c7c01fcf44e699c55fb80c3a0207067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882921ceb1ebf66ddfe7858a5fa4e84bd6cb0f65502e4174c26f4b2a89884362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:55:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 09 Aug 2022 17:55:30 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 17:55:31 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 09 Aug 2022 17:55:32 GMT
ENV APIFIREWALL_VERSION=v0.6.8
# Tue, 09 Aug 2022 17:55:35 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='af8e49e7ebf19d68b4dcf09a0f0b04b36a5c6e3f556549cb48852fcebac03892';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b15fa8bfb98d23760eac894002db79420cdc321c1f1baabf60fba54556dfdab7';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='d37c9cef562788caf0177224516c555808251a6d79a368b4902424d57037d023';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 09 Aug 2022 17:55:36 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 09 Aug 2022 17:55:36 GMT
USER api-firewall
# Tue, 09 Aug 2022 17:55:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 17:55:38 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0b06ab40d1b03f691e23f0fe6c3c6b188edc446bc077d8f2f86d33c65d105`  
		Last Modified: Tue, 09 Aug 2022 17:55:51 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432159dd21c8591ef96fc7bed539aa369ec6541012350355b9b681a46cb7348f`  
		Last Modified: Tue, 09 Aug 2022 17:55:52 GMT  
		Size: 4.5 MB (4538557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e24f95ec40bd2e6f5271b5993a7b38c86cc1198a4217a6c0f1a32b5ab7ebf80`  
		Last Modified: Tue, 09 Aug 2022 17:55:52 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:b540611885ccd5b45cec43f3816ee441d6fbe9ea05bb54f8a50351303dffb2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:c2ddf78dead8053c2fc2934c8596e081ac575a6f0fdd35f4824703681e3728f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7579923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2557517f85256294702dafbd88e3fb62c567277548bffe6ff868eb4ba657a36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:47:39 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 09 Aug 2022 17:47:39 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 17:47:39 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 09 Aug 2022 17:47:39 GMT
ENV APIFIREWALL_VERSION=v0.6.8
# Tue, 09 Aug 2022 17:47:41 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='af8e49e7ebf19d68b4dcf09a0f0b04b36a5c6e3f556549cb48852fcebac03892';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b15fa8bfb98d23760eac894002db79420cdc321c1f1baabf60fba54556dfdab7';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='d37c9cef562788caf0177224516c555808251a6d79a368b4902424d57037d023';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 09 Aug 2022 17:47:41 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 09 Aug 2022 17:47:41 GMT
USER api-firewall
# Tue, 09 Aug 2022 17:47:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 17:47:41 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e62924cbb5cae95f3719d409db2c9d3db9b2566cefe562b49879111b3c78b66`  
		Last Modified: Tue, 09 Aug 2022 17:47:49 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a238989c27ee4f9089df52b4f5af75ea74f4fae1d6a8d1586008974d67787`  
		Last Modified: Tue, 09 Aug 2022 17:47:50 GMT  
		Size: 4.8 MB (4754859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f619bbb80421d4f9885e17d2514dce73fb8adcd9dfc1aaec17f007a71dba1b`  
		Last Modified: Tue, 09 Aug 2022 17:47:49 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:ed0536610a9bbd163670ba0ad1ac4861705c0dbba724bedfe3dca8030fb7d3f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142522584cde6b75be3387a1ecd9d783050d295db84bf7e5c668aa64eb4d6fa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:56:18 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Jul 2022 22:56:19 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 22:56:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 19 Jul 2022 22:56:21 GMT
ENV APIFIREWALL_VERSION=v0.6.8
# Tue, 19 Jul 2022 22:56:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='af8e49e7ebf19d68b4dcf09a0f0b04b36a5c6e3f556549cb48852fcebac03892';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b15fa8bfb98d23760eac894002db79420cdc321c1f1baabf60fba54556dfdab7';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='d37c9cef562788caf0177224516c555808251a6d79a368b4902424d57037d023';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 19 Jul 2022 22:56:25 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 19 Jul 2022 22:56:25 GMT
USER api-firewall
# Tue, 19 Jul 2022 22:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 22:56:27 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dc8c65823421c8e5e29a6df3db37e534afb9f770dada80c22998c3595d7861`  
		Last Modified: Tue, 19 Jul 2022 22:56:40 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801b25042915e7ee577900b032e35a3158baf90dca58e59044ff040948a4c3a8`  
		Last Modified: Tue, 19 Jul 2022 22:56:41 GMT  
		Size: 4.5 MB (4460213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68464705dd22e8f9d0d2941db944bf97defa5f48dc63db331de5d196c191747`  
		Last Modified: Tue, 19 Jul 2022 22:56:41 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:1018c58d71d209d919edbefe6067b4797c7c01fcf44e699c55fb80c3a0207067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882921ceb1ebf66ddfe7858a5fa4e84bd6cb0f65502e4174c26f4b2a89884362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:55:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 09 Aug 2022 17:55:30 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 17:55:31 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 09 Aug 2022 17:55:32 GMT
ENV APIFIREWALL_VERSION=v0.6.8
# Tue, 09 Aug 2022 17:55:35 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='af8e49e7ebf19d68b4dcf09a0f0b04b36a5c6e3f556549cb48852fcebac03892';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b15fa8bfb98d23760eac894002db79420cdc321c1f1baabf60fba54556dfdab7';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='d37c9cef562788caf0177224516c555808251a6d79a368b4902424d57037d023';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 09 Aug 2022 17:55:36 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 09 Aug 2022 17:55:36 GMT
USER api-firewall
# Tue, 09 Aug 2022 17:55:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 17:55:38 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0b06ab40d1b03f691e23f0fe6c3c6b188edc446bc077d8f2f86d33c65d105`  
		Last Modified: Tue, 09 Aug 2022 17:55:51 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432159dd21c8591ef96fc7bed539aa369ec6541012350355b9b681a46cb7348f`  
		Last Modified: Tue, 09 Aug 2022 17:55:52 GMT  
		Size: 4.5 MB (4538557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e24f95ec40bd2e6f5271b5993a7b38c86cc1198a4217a6c0f1a32b5ab7ebf80`  
		Last Modified: Tue, 09 Aug 2022 17:55:52 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
