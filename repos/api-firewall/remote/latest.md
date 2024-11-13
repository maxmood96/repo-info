## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:50fdab4fd5efc5383780cd1d2ebd22d611d1df6ae28f0cb01923758a0aa1cfc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:6bc4e8899430af1ab737a83e31bbaaa898a7a8949ef8b70d5e7491e91682861c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14832175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c8721556bb35e715c40943241d67dce4fe422d9f8609df28bd8be1ff42fe4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 12 Nov 2024 20:20:50 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 12 Nov 2024 20:20:50 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 20:20:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 12 Nov 2024 20:20:50 GMT
ENV APIFIREWALL_VERSION=v0.8.4
# Tue, 12 Nov 2024 20:20:50 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='7abaef17f0c1a9d8129dd559607f8850ae3b7b8451151506d954272bc58948d5';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='2778b62f28aebd79af3b9125097d4c2455298a4aa777651e2a941d5425d8a1a5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='53cbc4b37060ebe11493b69c42962f2b9ef114f86d115c4c8ff7acd4761dc574';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 12 Nov 2024 20:20:50 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 12 Nov 2024 20:20:50 GMT
USER api-firewall
# Tue, 12 Nov 2024 20:20:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Nov 2024 20:20:50 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfda6ce0aad632cd64c19db86a35dadf40d8882a4a50c3a8b95e50684ed5549`  
		Last Modified: Tue, 12 Nov 2024 21:08:59 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5bb72ce617d5345ec884f295f1f3e89445b867e62077939fd1a08c51b6e530`  
		Last Modified: Tue, 12 Nov 2024 21:08:59 GMT  
		Size: 11.2 MB (11207006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdf2863e63e3be5cb8fccf4845dc63fbfa1c1a3ee77777a3c282c04bff69812`  
		Last Modified: Tue, 12 Nov 2024 21:09:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:71e084663c4118ffe1c89dd6c6a612ee0213e1ca47c01cc72156ace7868e5925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bc85e9a8c63e758b7c3cf562bc065d9a9a040e39e6772ec29c099c641cc6ee`

```dockerfile
```

-	Layers:
	-	`sha256:126a3b3cfe816ba796002074fc5d3f83e511f1ed77aa34e7ab87659a0d0c47c8`  
		Last Modified: Tue, 12 Nov 2024 21:08:59 GMT  
		Size: 13.3 KB (13330 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:14e41f2638f7f95e90cb255a3a8028562c11e219f040b4b6f9a00c64523012e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14461281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a3d8738b00387d7dbd8f814b49986ce1212240d786e5ad4406707e730fa3df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 05:33:11 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 28 Oct 2024 05:33:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 05:33:11 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 28 Oct 2024 05:33:11 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 05:33:11 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 28 Oct 2024 05:33:11 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 28 Oct 2024 05:33:11 GMT
USER api-firewall
# Mon, 28 Oct 2024 05:33:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 05:33:11 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24d370984f79462d48466cdaf28bb698b9ed8ef1b1b00f0b08b857ef7fd8c8d`  
		Last Modified: Tue, 12 Nov 2024 02:01:43 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80662c63d214b3e2e4b59941efb4b7bfb4bd392c7c1058ff98b852199232583`  
		Last Modified: Tue, 12 Nov 2024 02:01:43 GMT  
		Size: 10.4 MB (10372287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bef7d994f48fd24d7e7ad1692e32150d043542898df112f3fb7655503fcde`  
		Last Modified: Tue, 12 Nov 2024 02:01:43 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:e0c0e1d30d3aa98428ef34ce475286bc6a96cb67db402d48a038fdb15e4cc18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23599cfe343bcc49dcc9d5145012831d607ce1a325fa840731d0b96f7945213d`

```dockerfile
```

-	Layers:
	-	`sha256:ee93010f99f5f8f824833478ac1356317a6dd07117fe7a168c7a3fe9dda4de71`  
		Last Modified: Tue, 12 Nov 2024 02:01:43 GMT  
		Size: 13.4 KB (13426 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:f4041f4c8a8d07b67bd3495dc007d84c8ddc0d57c815ba94ac2927f42895f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13198621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4edfe3bc6e53fac32e2ba5d25895eb1d30551010814f6161686dfc412946901`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 12 Nov 2024 20:20:50 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 12 Nov 2024 20:20:50 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 20:20:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 12 Nov 2024 20:20:50 GMT
ENV APIFIREWALL_VERSION=v0.8.4
# Tue, 12 Nov 2024 20:20:50 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='7abaef17f0c1a9d8129dd559607f8850ae3b7b8451151506d954272bc58948d5';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='2778b62f28aebd79af3b9125097d4c2455298a4aa777651e2a941d5425d8a1a5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='53cbc4b37060ebe11493b69c42962f2b9ef114f86d115c4c8ff7acd4761dc574';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 12 Nov 2024 20:20:50 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 12 Nov 2024 20:20:50 GMT
USER api-firewall
# Tue, 12 Nov 2024 20:20:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Nov 2024 20:20:50 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2841ad4a368826e9cd0e528de3de79958bf3cc3b837196e70cf8f9e71968c41c`  
		Last Modified: Tue, 12 Nov 2024 21:09:05 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e6383c129e50db689126bd42279fb560b8a80c4ade4f14b4799cbc9bf71c9f`  
		Last Modified: Tue, 12 Nov 2024 21:09:05 GMT  
		Size: 9.7 MB (9728137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8cb9c66a5cd36df047db1cdee1436a95c44b49c7d64ab20dabbd3a8ba27e04`  
		Last Modified: Tue, 12 Nov 2024 21:09:05 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:916f851ee63cec96bf810dad5cf700f3c8d0d8fcb021dfa53348d53c2e5c26b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd24523842320aae8b8e637320002703460b6bc805205a8e6f38cb4331c9b0`

```dockerfile
```

-	Layers:
	-	`sha256:ffdcb38c79c7b437b698bd9e3bb775995e0156eff961695b7db989535ecd6c85`  
		Last Modified: Tue, 12 Nov 2024 21:09:05 GMT  
		Size: 13.3 KB (13305 bytes)  
		MIME: application/vnd.in-toto+json
