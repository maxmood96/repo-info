<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.8.4`](#api-firewall084)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.8.4`

```console
$ docker pull api-firewall@sha256:d829118f6ff75c74c62666fca1eeb4d28f8aaf6022e4b57ea893166b4f2a8ef0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.8.4` - linux; amd64

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

### `api-firewall:0.8.4` - unknown; unknown

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

### `api-firewall:0.8.4` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:697bc92815b6172aacaf00835f3e70fc6eeddd1146629967830a3059515bc079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14442522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d222594a1091033c9ad3527667a3d70e793fb6d784999e006de3b55cd0c78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704bdb1084bce793fd1beefd9a1fc4347d4007576b7611b9a23d27fecd613fa0`  
		Last Modified: Wed, 13 Nov 2024 01:50:59 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0c8386fb012d2a86b12848424559e451510c89894c82d7e8e135f8dd0ec67`  
		Last Modified: Wed, 13 Nov 2024 01:51:00 GMT  
		Size: 10.4 MB (10353534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3074e4ed5b56dcc83c1e5a9eff22db3c7f9f542b7f2cb7f341360c1176b7f40`  
		Last Modified: Wed, 13 Nov 2024 01:50:59 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.8.4` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2b4a187ea064b7eccbae849f1be057e8872e9c27acdf6737f4b3302082125ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31f432ce31cb3d6ec4c0cdcbb5bbd33d801c7711bab6f81e295da88c4b30e38`

```dockerfile
```

-	Layers:
	-	`sha256:889e5fc117943123cd2354379bfd27ba4971a4f9baf3e462b40f0187a3e4cc63`  
		Last Modified: Wed, 13 Nov 2024 01:50:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.8.4` - linux; 386

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

### `api-firewall:0.8.4` - unknown; unknown

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

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d829118f6ff75c74c62666fca1eeb4d28f8aaf6022e4b57ea893166b4f2a8ef0
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
$ docker pull api-firewall@sha256:697bc92815b6172aacaf00835f3e70fc6eeddd1146629967830a3059515bc079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14442522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d222594a1091033c9ad3527667a3d70e793fb6d784999e006de3b55cd0c78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704bdb1084bce793fd1beefd9a1fc4347d4007576b7611b9a23d27fecd613fa0`  
		Last Modified: Wed, 13 Nov 2024 01:50:59 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0c8386fb012d2a86b12848424559e451510c89894c82d7e8e135f8dd0ec67`  
		Last Modified: Wed, 13 Nov 2024 01:51:00 GMT  
		Size: 10.4 MB (10353534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3074e4ed5b56dcc83c1e5a9eff22db3c7f9f542b7f2cb7f341360c1176b7f40`  
		Last Modified: Wed, 13 Nov 2024 01:50:59 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2b4a187ea064b7eccbae849f1be057e8872e9c27acdf6737f4b3302082125ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31f432ce31cb3d6ec4c0cdcbb5bbd33d801c7711bab6f81e295da88c4b30e38`

```dockerfile
```

-	Layers:
	-	`sha256:889e5fc117943123cd2354379bfd27ba4971a4f9baf3e462b40f0187a3e4cc63`  
		Last Modified: Wed, 13 Nov 2024 01:50:59 GMT  
		Size: 13.4 KB (13424 bytes)  
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
