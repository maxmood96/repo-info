<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.7.3`](#api-firewall073)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.7.3`

**does not exist** (yet?)

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:9e9f0374b97c9f4ac63dbb702d4e1f776bc8488ade58ff4bf83922304f018770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:1f4f679e3b3e3cec24eeaf6e8bd2d126fdbb9b84c223db0580a2a23cd6c08002
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14196600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ff214038079d3823de64a06957442946da5cab2f304d1bab1f31775e94584b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:58:15 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 16 Mar 2024 07:58:15 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 07:58:15 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 17 Apr 2024 17:51:19 GMT
ENV APIFIREWALL_VERSION=v0.7.2
# Wed, 17 Apr 2024 17:51:22 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d37f804498472459ac9e974093d767fb3944c46e6db325a98917b249e063dff0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='23a202516b26219e250b2adb1e7a905795e91003dadd6209c72ca9c737085481';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8b3a5b335c4fb6d14ff159875178826dd4e80a10ec3de26ca42ab1ed30123536';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 17 Apr 2024 17:51:22 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 17 Apr 2024 17:51:22 GMT
USER api-firewall
# Wed, 17 Apr 2024 17:51:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Apr 2024 17:51:23 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996bf125e6b3d4ba812c8d06e1edb5c9b93b9afcf0b23a4b46709f99f65a1ef0`  
		Last Modified: Sat, 16 Mar 2024 07:58:26 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926f4c1535895073f24a02e9dde0267c269a3119eef996b519eff49e5ef70fd6`  
		Last Modified: Wed, 17 Apr 2024 17:51:39 GMT  
		Size: 10.8 MB (10792496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cce0eb0be60df72eb53ced20cc81b9a24d6feee98389c5058245d819069bcdb`  
		Last Modified: Wed, 17 Apr 2024 17:51:38 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:b404a8db7b31974364628b43b84b8b33fc0f96effd3d0b8a753148d832feb23f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13292559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0afd76ad459b807b9d9a0d20b9c09700b8d6022240673f40405582e2a6b44dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:04 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 16 Mar 2024 02:53:04 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 02:53:04 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 17 Apr 2024 18:03:43 GMT
ENV APIFIREWALL_VERSION=v0.7.2
# Wed, 17 Apr 2024 18:03:46 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d37f804498472459ac9e974093d767fb3944c46e6db325a98917b249e063dff0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='23a202516b26219e250b2adb1e7a905795e91003dadd6209c72ca9c737085481';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8b3a5b335c4fb6d14ff159875178826dd4e80a10ec3de26ca42ab1ed30123536';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 17 Apr 2024 18:03:46 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 17 Apr 2024 18:03:46 GMT
USER api-firewall
# Wed, 17 Apr 2024 18:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Apr 2024 18:03:46 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aae77be32174ba91ba46eef23ccdaeed963df0e51624d178421140648cb98b`  
		Last Modified: Sat, 16 Mar 2024 02:53:16 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeeb9e11a29bd9b19e98fb6da66beee3a58648894c2777fac969096572bd323`  
		Last Modified: Wed, 17 Apr 2024 18:04:02 GMT  
		Size: 10.0 MB (9957634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a546b976dec4bc59c31294c0ebd0d31d5c1ad4ba959a89ee41daf81b7f04778`  
		Last Modified: Wed, 17 Apr 2024 18:04:01 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:44034f065c29ccb89c7e4815834bc6a23ffac601bf3c9b12937f28699a8f2932
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12600818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1d6c3aab6191d22bed77ec8756f60a76a2efa2114e9e33d57c13966d7d661a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:52:59 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Mar 2024 23:52:59 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 23:52:59 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 17 Apr 2024 16:57:32 GMT
ENV APIFIREWALL_VERSION=v0.7.2
# Wed, 17 Apr 2024 16:57:34 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d37f804498472459ac9e974093d767fb3944c46e6db325a98917b249e063dff0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='23a202516b26219e250b2adb1e7a905795e91003dadd6209c72ca9c737085481';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8b3a5b335c4fb6d14ff159875178826dd4e80a10ec3de26ca42ab1ed30123536';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 17 Apr 2024 16:57:35 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 17 Apr 2024 16:57:35 GMT
USER api-firewall
# Wed, 17 Apr 2024 16:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Apr 2024 16:57:35 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b16feb1c089d261f25d668bc94fb450ae9faaf09472431fb07eaa76ff9fb84`  
		Last Modified: Fri, 15 Mar 2024 23:53:10 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d59d88d4f1f263566209360673e06457c8b2ac183a93217acbfeec21fe3840`  
		Last Modified: Wed, 17 Apr 2024 16:57:53 GMT  
		Size: 9.4 MB (9360193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43679e87d99bf6649bee777299b0405c2fea2af549d7d89ee84d703eedc74944`  
		Last Modified: Wed, 17 Apr 2024 16:57:51 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
