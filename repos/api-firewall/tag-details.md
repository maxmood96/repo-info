<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.3`](#api-firewall093)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.3`

```console
$ docker pull api-firewall@sha256:8d3dbe4021cbabd0b616fe704c1d9b582ca5275f80603a56c15d853c89ec9e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.9.3` - linux; amd64

```console
$ docker pull api-firewall@sha256:5b75b66f6e40e67c712e7e865a336e3bef10308366eb75964e95e015824afdb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17153027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc34b9f2cd8cc6a6c520a762a139a4554bdd1b5eb9b07734025cc84fee6a5aeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9ac3c0e69c945b65a15f7d7f697ab865f6d0534f11e6b56dc8b72a6e669d7c`  
		Last Modified: Tue, 19 Aug 2025 16:52:01 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7afd62a09bbb5a8071c3ed0be547aefbca06cf6887e3ddd9c7b55e862fab7aa`  
		Last Modified: Tue, 19 Aug 2025 16:52:02 GMT  
		Size: 13.4 MB (13352086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eb6c8e3b1de0bd39fe819618fcb0d8ce2d1282726ba60d284f6aab469150b3`  
		Last Modified: Tue, 19 Aug 2025 16:52:01 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.3` - unknown; unknown

```console
$ docker pull api-firewall@sha256:3b3e1fdf1e7cd38b2b5fb67bd049aa4f36074a0db87a76c25f9765668fe5f10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512249f58c056cd538f6aa00e85166ac1c8f622a3641a9c11905fa3b81db6183`

```dockerfile
```

-	Layers:
	-	`sha256:52c52fac710ac2a3e99e26d5a1c1dc627b701631b25ccf37463b0ce81708eb66`  
		Last Modified: Tue, 19 Aug 2025 17:44:25 GMT  
		Size: 164.6 KB (164574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3abd8cc069877f715edc77be17a037662e0137fc2ffff8f726d73263cb33445`  
		Last Modified: Tue, 19 Aug 2025 17:44:25 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.3` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:f4145e293e50032589fef46e34cf97aa489b5983e0c239f556c5cc88dc91ddf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16423628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62601edd0e88ae1fa7eabd176e0021bebad7d25773470b8e6095d94796d88a65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e230637c00bf0228059e5d3879e0d94fb421c1114d2d3f417ea12fa6131b2`  
		Last Modified: Tue, 19 Aug 2025 17:07:53 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51ed03b8e1b35be66c41b0c09c09767bfdfaf85deffa1fa895034dfd8cec877`  
		Last Modified: Tue, 19 Aug 2025 17:07:54 GMT  
		Size: 12.3 MB (12291628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848bed6b37bd4b47068cb095da5aebfe890d6c9111ac694dd7d4b49b9270d140`  
		Last Modified: Tue, 19 Aug 2025 17:07:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.3` - unknown; unknown

```console
$ docker pull api-firewall@sha256:0115f3256f630819a47be00ec3fc722821d677f2dda08d7a52434abd33dc4fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 KB (178247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87072cc63bb3cf16c287f1cc6e0fc4391741cf385f796ee11de063280f57312`

```dockerfile
```

-	Layers:
	-	`sha256:f1d839f7af8f5503b6363f58b90c582883bb2021e0f95b090e91def99c946d98`  
		Last Modified: Tue, 19 Aug 2025 17:44:29 GMT  
		Size: 164.6 KB (164606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e342a1f532eef4e4f740c20eb36da8b703ce9aa6cc922c16c434d12f920648`  
		Last Modified: Tue, 19 Aug 2025 17:44:30 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.3` - linux; 386

```console
$ docker pull api-firewall@sha256:11dac54710f66232830ddb98e60f05c98a5e9fdf3461bb1191caf53789fd23fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869db2311ba3013e4856f7da56780f18c96f83f39642d2d9a8651ff667038c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25ff2d222e9d8bf9b0e989f5027175891d1d86d7b163bdfe0f7c6659cb1edc7`  
		Last Modified: Tue, 19 Aug 2025 16:53:11 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b907a238551b4b27c579b5db0e5d232dd32ff746ee7ab8382f77be2de3e53ecc`  
		Last Modified: Tue, 19 Aug 2025 16:53:11 GMT  
		Size: 11.8 MB (11821048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce461b5702b3b629245cf25a39136d0e00a1ef1e12b0cb8cc31f3c700888adee`  
		Last Modified: Tue, 19 Aug 2025 16:53:11 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.3` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2a28c26969908bfb0599bea60037d5338f77e8389e735bc1ff19f6a1996cbb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59308c18c30644bce9b0bb0be0680e5f9efa70a32b2da0145ce1ad6e9eaca092`

```dockerfile
```

-	Layers:
	-	`sha256:2538e3438bd0844feeda0a0ad67a6dcdd841c7bf244a067caa7697097108e8bf`  
		Last Modified: Tue, 19 Aug 2025 17:44:33 GMT  
		Size: 164.6 KB (164559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db34cde316c2bea01fe126595325aa04b1ed615226c5f8e4cf82e340759af0d`  
		Last Modified: Tue, 19 Aug 2025 17:44:34 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:8d3dbe4021cbabd0b616fe704c1d9b582ca5275f80603a56c15d853c89ec9e67
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
$ docker pull api-firewall@sha256:5b75b66f6e40e67c712e7e865a336e3bef10308366eb75964e95e015824afdb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17153027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc34b9f2cd8cc6a6c520a762a139a4554bdd1b5eb9b07734025cc84fee6a5aeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9ac3c0e69c945b65a15f7d7f697ab865f6d0534f11e6b56dc8b72a6e669d7c`  
		Last Modified: Tue, 19 Aug 2025 16:52:01 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7afd62a09bbb5a8071c3ed0be547aefbca06cf6887e3ddd9c7b55e862fab7aa`  
		Last Modified: Tue, 19 Aug 2025 16:52:02 GMT  
		Size: 13.4 MB (13352086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eb6c8e3b1de0bd39fe819618fcb0d8ce2d1282726ba60d284f6aab469150b3`  
		Last Modified: Tue, 19 Aug 2025 16:52:01 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:3b3e1fdf1e7cd38b2b5fb67bd049aa4f36074a0db87a76c25f9765668fe5f10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512249f58c056cd538f6aa00e85166ac1c8f622a3641a9c11905fa3b81db6183`

```dockerfile
```

-	Layers:
	-	`sha256:52c52fac710ac2a3e99e26d5a1c1dc627b701631b25ccf37463b0ce81708eb66`  
		Last Modified: Tue, 19 Aug 2025 17:44:25 GMT  
		Size: 164.6 KB (164574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3abd8cc069877f715edc77be17a037662e0137fc2ffff8f726d73263cb33445`  
		Last Modified: Tue, 19 Aug 2025 17:44:25 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:f4145e293e50032589fef46e34cf97aa489b5983e0c239f556c5cc88dc91ddf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16423628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62601edd0e88ae1fa7eabd176e0021bebad7d25773470b8e6095d94796d88a65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e230637c00bf0228059e5d3879e0d94fb421c1114d2d3f417ea12fa6131b2`  
		Last Modified: Tue, 19 Aug 2025 17:07:53 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51ed03b8e1b35be66c41b0c09c09767bfdfaf85deffa1fa895034dfd8cec877`  
		Last Modified: Tue, 19 Aug 2025 17:07:54 GMT  
		Size: 12.3 MB (12291628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848bed6b37bd4b47068cb095da5aebfe890d6c9111ac694dd7d4b49b9270d140`  
		Last Modified: Tue, 19 Aug 2025 17:07:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:0115f3256f630819a47be00ec3fc722821d677f2dda08d7a52434abd33dc4fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 KB (178247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87072cc63bb3cf16c287f1cc6e0fc4391741cf385f796ee11de063280f57312`

```dockerfile
```

-	Layers:
	-	`sha256:f1d839f7af8f5503b6363f58b90c582883bb2021e0f95b090e91def99c946d98`  
		Last Modified: Tue, 19 Aug 2025 17:44:29 GMT  
		Size: 164.6 KB (164606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e342a1f532eef4e4f740c20eb36da8b703ce9aa6cc922c16c434d12f920648`  
		Last Modified: Tue, 19 Aug 2025 17:44:30 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:11dac54710f66232830ddb98e60f05c98a5e9fdf3461bb1191caf53789fd23fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869db2311ba3013e4856f7da56780f18c96f83f39642d2d9a8651ff667038c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25ff2d222e9d8bf9b0e989f5027175891d1d86d7b163bdfe0f7c6659cb1edc7`  
		Last Modified: Tue, 19 Aug 2025 16:53:11 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b907a238551b4b27c579b5db0e5d232dd32ff746ee7ab8382f77be2de3e53ecc`  
		Last Modified: Tue, 19 Aug 2025 16:53:11 GMT  
		Size: 11.8 MB (11821048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce461b5702b3b629245cf25a39136d0e00a1ef1e12b0cb8cc31f3c700888adee`  
		Last Modified: Tue, 19 Aug 2025 16:53:11 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2a28c26969908bfb0599bea60037d5338f77e8389e735bc1ff19f6a1996cbb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59308c18c30644bce9b0bb0be0680e5f9efa70a32b2da0145ce1ad6e9eaca092`

```dockerfile
```

-	Layers:
	-	`sha256:2538e3438bd0844feeda0a0ad67a6dcdd841c7bf244a067caa7697097108e8bf`  
		Last Modified: Tue, 19 Aug 2025 17:44:33 GMT  
		Size: 164.6 KB (164559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db34cde316c2bea01fe126595325aa04b1ed615226c5f8e4cf82e340759af0d`  
		Last Modified: Tue, 19 Aug 2025 17:44:34 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json
