<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.3`](#api-firewall093)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.3`

**does not exist** (yet?)

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d206d69e251fe1c8fed16f7db855f82e794b1505f5922db05e29aae384db29b8
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
$ docker pull api-firewall@sha256:fb64e75d63fcfc516bb2d7fa95362a3bba4726118b030c28d702ff0e72e3faab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16905782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672ca36d650fcd1df7d5a16a76a87eaff4dea288cf67d8a634930efd8d1b9fa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 17:35:47 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Aug 2025 17:35:47 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 17:35:47 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
ENV APIFIREWALL_VERSION=v0.9.2
# Fri, 15 Aug 2025 17:35:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='30f2091a48d8ac7257c701259a1ffd484bb96306cd7e3610ebbdfee8455e0919';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='ade1ee8a322fca4a59e2b9bfe83dfbad88efcf0a99ed0b714b43869d454d8601';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8cbad671b2282dbc04e6924c1c7f3233c0d1f08aa7f3c6ee86cb4d32682fa905';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
USER api-firewall
# Fri, 15 Aug 2025 17:35:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Aug 2025 17:35:47 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1567085973aef116f98708b21661ad847d1b00283a524a52389d8f14ea6b6f5c`  
		Last Modified: Fri, 15 Aug 2025 18:36:31 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a770b8a75f22c99ff793041e956a7c240482089d25fc1807b52bbf47a1e6e26b`  
		Last Modified: Fri, 15 Aug 2025 18:36:32 GMT  
		Size: 13.1 MB (13104846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f172e58d7ebe3f14f791596d23b17c40c64483fd88148b4e436bd60b1d6ca45b`  
		Last Modified: Fri, 15 Aug 2025 18:35:52 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:b9fb8d8f1647ef51268c26fb795d6fded9e7e460e75395117b63494f8e8ab73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a58ca2a2f47e7b1c7c0c6c111105126c3cc1091f3f912073e6e7674ab0063d`

```dockerfile
```

-	Layers:
	-	`sha256:2647782bb8fa3e16cb1cfb3cc818274146d95d7d3eb26fde5182ba3fbd9ff699`  
		Last Modified: Fri, 15 Aug 2025 20:44:31 GMT  
		Size: 164.6 KB (164580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c0079463fcff84268c0c8e13dca1871bceddf9bb2816783b19612b64f82147`  
		Last Modified: Fri, 15 Aug 2025 20:44:32 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:4f7258fd3f317a7e1825c5a379fedfb48d975f61c195d4cbd5624a37e0c991f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16224066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a79a426950dcacd0c99c3114add92d86477a78b972392744bd1751195d724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 17:35:47 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Aug 2025 17:35:47 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 17:35:47 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
ENV APIFIREWALL_VERSION=v0.9.2
# Fri, 15 Aug 2025 17:35:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='30f2091a48d8ac7257c701259a1ffd484bb96306cd7e3610ebbdfee8455e0919';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='ade1ee8a322fca4a59e2b9bfe83dfbad88efcf0a99ed0b714b43869d454d8601';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8cbad671b2282dbc04e6924c1c7f3233c0d1f08aa7f3c6ee86cb4d32682fa905';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
USER api-firewall
# Fri, 15 Aug 2025 17:35:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Aug 2025 17:35:47 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c76f1bfc3f5cedd718bb2de97ab201c2f5efc2b4ccc60ab4fde42f8011834a`  
		Last Modified: Fri, 15 Aug 2025 19:53:46 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca52d9a7d4601cbb60c3ce5b026d836e70a993cc5d1ebe879ad74c3e102836f`  
		Last Modified: Fri, 15 Aug 2025 19:53:48 GMT  
		Size: 12.1 MB (12092070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc31f95ce45c0b6062d72f94d4d6e0352e76942501d0122c3a1deef2a0bee3ac`  
		Last Modified: Fri, 15 Aug 2025 19:53:45 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:d254545222e62fa85f0af60103576037be409a0c9d6ad0e9e741c0d4392247a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 KB (178253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ef28166d27534f19bdaddc8a3caa3c6e1a705121798651b6897949bfd5332a`

```dockerfile
```

-	Layers:
	-	`sha256:defa69a721ec58579b9b829ce0a8ad6714ebb3f13ee8f895c6e84263a720462e`  
		Last Modified: Fri, 15 Aug 2025 20:44:35 GMT  
		Size: 164.6 KB (164612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890bdc0e86fa00d6347f3bf7e154e5602a3dfabf3c4a7df2d9262c10f041754a`  
		Last Modified: Fri, 15 Aug 2025 20:44:36 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:17110de8df21a6e695cb0524234650dc23e20f14d3cd108ce16b95334ca7dd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15129508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ced1e496b789335c8a4dacff24dd9008db39ab4c745c163c7aafc88e21e0060`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 17:35:47 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Aug 2025 17:35:47 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 17:35:47 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
ENV APIFIREWALL_VERSION=v0.9.2
# Fri, 15 Aug 2025 17:35:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='30f2091a48d8ac7257c701259a1ffd484bb96306cd7e3610ebbdfee8455e0919';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='ade1ee8a322fca4a59e2b9bfe83dfbad88efcf0a99ed0b714b43869d454d8601';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8cbad671b2282dbc04e6924c1c7f3233c0d1f08aa7f3c6ee86cb4d32682fa905';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 15 Aug 2025 17:35:47 GMT
USER api-firewall
# Fri, 15 Aug 2025 17:35:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Aug 2025 17:35:47 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c456c69a0b0015390e40112d9c41ccf15fbf1cf5ed543e81cde6df96e6f08b1`  
		Last Modified: Fri, 15 Aug 2025 18:35:52 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe35bcc0b908f1f420d7917a33f215224d4669ed76faba6c6dfbfd5f5d4fcfb`  
		Last Modified: Fri, 15 Aug 2025 18:35:54 GMT  
		Size: 11.5 MB (11513256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f172e58d7ebe3f14f791596d23b17c40c64483fd88148b4e436bd60b1d6ca45b`  
		Last Modified: Fri, 15 Aug 2025 18:35:52 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:61a690b6e435dfe299bf772714d08e538de0cb2513824f4cb72acd32754d6662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbbdd3b97408091280b7e1c7170462c62fc9946e29cf10e3d10a9e3677b1fff`

```dockerfile
```

-	Layers:
	-	`sha256:66b5f2d94254c5f49c555d66aefa4b8650853724ece8b40475d2a22ccd3fbaf1`  
		Last Modified: Fri, 15 Aug 2025 20:44:40 GMT  
		Size: 164.6 KB (164565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3d2c73a134574ec9bdf3845ba74f399b0e43186fcb89b96731ec825783abdc`  
		Last Modified: Fri, 15 Aug 2025 20:44:40 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json
