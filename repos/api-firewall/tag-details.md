<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.4`](#api-firewall094)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.4`

```console
$ docker pull api-firewall@sha256:6f9d0a5ddab241ef969c8454c8f988cfebdeff39dc22fce4cfc0fffbdb8a5326
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.9.4` - linux; amd64

```console
$ docker pull api-firewall@sha256:e485b23b8f23ef9342588035f73aa56fbc8cc6376bd0a2b772f5b067b84ae3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17397908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0265a524076201323ee61375745e66feea23e29281f0957d9284e95395258ed0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 23:06:16 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 01 Dec 2025 23:06:16 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:06:16 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 01 Dec 2025 23:06:16 GMT
ENV APIFIREWALL_VERSION=v0.9.4
# Mon, 01 Dec 2025 23:06:17 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='89c7d5ebcb35733c90b1adee529f7116adf7880311706029d2470af792176e0c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f8590efca3d526ea3b0a85b245bbdbb647bebcb01fcbc5bafeff03b81a479a70';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='90ac4e0c2b864e24e87b85f9012ff9c67ed5ae807828bc61ec4d5c6c30e6fabc';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 01 Dec 2025 23:06:17 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 01 Dec 2025 23:06:17 GMT
USER api-firewall
# Mon, 01 Dec 2025 23:06:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:06:17 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53f6955a28a799440efc05bc2c0822bcc70c489913f0174efd00a7a7c24cdb9`  
		Last Modified: Mon, 01 Dec 2025 23:06:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fc8acc3549d1447b82d2efeb97894582bdf40df31ac8e7d54d2a01e7370db2`  
		Last Modified: Mon, 01 Dec 2025 23:06:44 GMT  
		Size: 13.6 MB (13594203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecee1fae3bdd8ee49eac8b4ec9c1acad2ca7df25d932c52422da7908e63791`  
		Last Modified: Mon, 01 Dec 2025 23:06:42 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.4` - unknown; unknown

```console
$ docker pull api-firewall@sha256:df60dde07d9e5f404540efb312d23136d56580f0232ae9ba2366062f0b0d7d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccf86cb6ebbe4deb7db04c16f055d230177bfda3d90395f48708b4bc9090271`

```dockerfile
```

-	Layers:
	-	`sha256:7aa96f4f72ebe85593e01b52fcf9f924cc43cf19c3f60d298a10c5c28cd80756`  
		Last Modified: Tue, 02 Dec 2025 00:44:32 GMT  
		Size: 167.0 KB (166989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:294ac7084beeb5d4c282973413dc94cc9fff1ff1c3933021c4022dd2f51b3f28`  
		Last Modified: Tue, 02 Dec 2025 00:44:33 GMT  
		Size: 13.5 KB (13503 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.4` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:4b3f3d64d4479ae0c66466fb3b3caae5e7af2c30bbbfc3a4cb993c2c387813af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16641520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1163ff3ee0cced91b11c1885e3007fdc1fc42dca2de2ad55e338216325ae28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 22:50:43 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 01 Dec 2025 22:50:43 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 22:50:43 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 01 Dec 2025 22:50:43 GMT
ENV APIFIREWALL_VERSION=v0.9.4
# Mon, 01 Dec 2025 22:50:45 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='89c7d5ebcb35733c90b1adee529f7116adf7880311706029d2470af792176e0c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f8590efca3d526ea3b0a85b245bbdbb647bebcb01fcbc5bafeff03b81a479a70';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='90ac4e0c2b864e24e87b85f9012ff9c67ed5ae807828bc61ec4d5c6c30e6fabc';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 01 Dec 2025 22:50:45 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 01 Dec 2025 22:50:45 GMT
USER api-firewall
# Mon, 01 Dec 2025 22:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 22:50:45 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f70c60ef0bbe229a41d4d6bfacb0f0cea472a409b0442f3d8094d25857abfe5`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fad9856cbbaf6ef2fd95ba1ea5a37225d3b7901592d872f86ff0439aff5bcc`  
		Last Modified: Mon, 01 Dec 2025 22:51:11 GMT  
		Size: 12.5 MB (12502197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4bc2a3ea4af565986bb5e92c0b1b6d35b484e4549e03a45ee560d600e222ed`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.4` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2112c4e911ae873048340b999ce63635d9a4d35fd4e703d0042269130a315279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 KB (180618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6005ce27c628ac7875e9335475a0ebc0256de83a7d663cbc32e9fa535404bc`

```dockerfile
```

-	Layers:
	-	`sha256:aefdd50c3bbc9d11a7fc27ea0e862a1d9ecca4ab9e599e2294e0c39363393e83`  
		Last Modified: Tue, 02 Dec 2025 00:44:36 GMT  
		Size: 167.0 KB (167021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77da1addb1bb0e592824846a1414955241bf6f88ef6e09801aeeff502ff3a4ad`  
		Last Modified: Tue, 02 Dec 2025 00:44:37 GMT  
		Size: 13.6 KB (13597 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.4` - linux; 386

```console
$ docker pull api-firewall@sha256:b610b5a218bd353c0c0db2973caaad1f65a5cde3bc7a20ee9fa264820ed2d1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15674312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c01dd3a966341ee9395a421b9ed4609e9b4aa7ba57a67d76b41b19b049dff6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 22:50:50 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 01 Dec 2025 22:50:50 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 22:50:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 01 Dec 2025 22:50:50 GMT
ENV APIFIREWALL_VERSION=v0.9.4
# Mon, 01 Dec 2025 22:50:52 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='89c7d5ebcb35733c90b1adee529f7116adf7880311706029d2470af792176e0c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f8590efca3d526ea3b0a85b245bbdbb647bebcb01fcbc5bafeff03b81a479a70';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='90ac4e0c2b864e24e87b85f9012ff9c67ed5ae807828bc61ec4d5c6c30e6fabc';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 01 Dec 2025 22:50:52 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 01 Dec 2025 22:50:52 GMT
USER api-firewall
# Mon, 01 Dec 2025 22:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 22:50:52 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da609a601a76b0fc61ac747b2ce4262b5a05dddbf491061e69010944542a7e60`  
		Last Modified: Mon, 01 Dec 2025 22:51:11 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b9a01ab00363fcc1624dd04b86cf34db0440700f630f09949493d79d9e45b2`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 12.1 MB (12054129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249addff1b82caaee61ffc39280ff27a01bf2128af5b85777e5d4d5398751e31`  
		Last Modified: Mon, 01 Dec 2025 22:51:11 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.4` - unknown; unknown

```console
$ docker pull api-firewall@sha256:4415fa2a3788c7670b8291a0a3d75d56584218ba6639ce73c6d984a78ee4cc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1a0fb3a53d2cd2a7a2fab74246ad54c87fe4790e537af8f6b5c4ebea305ce0`

```dockerfile
```

-	Layers:
	-	`sha256:7e33db088ab5d193f3014abc161b5ac547fb22308af7f0f0d352fc4ecbbfdfa3`  
		Last Modified: Tue, 02 Dec 2025 00:44:40 GMT  
		Size: 167.0 KB (166974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda890e8ff5752f5e00b250dba39b4b2a54b89fabc595c694b3786a19e8232d7`  
		Last Modified: Tue, 02 Dec 2025 00:44:41 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:6f9d0a5ddab241ef969c8454c8f988cfebdeff39dc22fce4cfc0fffbdb8a5326
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
$ docker pull api-firewall@sha256:e485b23b8f23ef9342588035f73aa56fbc8cc6376bd0a2b772f5b067b84ae3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17397908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0265a524076201323ee61375745e66feea23e29281f0957d9284e95395258ed0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 23:06:16 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 01 Dec 2025 23:06:16 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:06:16 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 01 Dec 2025 23:06:16 GMT
ENV APIFIREWALL_VERSION=v0.9.4
# Mon, 01 Dec 2025 23:06:17 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='89c7d5ebcb35733c90b1adee529f7116adf7880311706029d2470af792176e0c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f8590efca3d526ea3b0a85b245bbdbb647bebcb01fcbc5bafeff03b81a479a70';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='90ac4e0c2b864e24e87b85f9012ff9c67ed5ae807828bc61ec4d5c6c30e6fabc';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 01 Dec 2025 23:06:17 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 01 Dec 2025 23:06:17 GMT
USER api-firewall
# Mon, 01 Dec 2025 23:06:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:06:17 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53f6955a28a799440efc05bc2c0822bcc70c489913f0174efd00a7a7c24cdb9`  
		Last Modified: Mon, 01 Dec 2025 23:06:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fc8acc3549d1447b82d2efeb97894582bdf40df31ac8e7d54d2a01e7370db2`  
		Last Modified: Mon, 01 Dec 2025 23:06:44 GMT  
		Size: 13.6 MB (13594203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecee1fae3bdd8ee49eac8b4ec9c1acad2ca7df25d932c52422da7908e63791`  
		Last Modified: Mon, 01 Dec 2025 23:06:42 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:df60dde07d9e5f404540efb312d23136d56580f0232ae9ba2366062f0b0d7d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccf86cb6ebbe4deb7db04c16f055d230177bfda3d90395f48708b4bc9090271`

```dockerfile
```

-	Layers:
	-	`sha256:7aa96f4f72ebe85593e01b52fcf9f924cc43cf19c3f60d298a10c5c28cd80756`  
		Last Modified: Tue, 02 Dec 2025 00:44:32 GMT  
		Size: 167.0 KB (166989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:294ac7084beeb5d4c282973413dc94cc9fff1ff1c3933021c4022dd2f51b3f28`  
		Last Modified: Tue, 02 Dec 2025 00:44:33 GMT  
		Size: 13.5 KB (13503 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:4b3f3d64d4479ae0c66466fb3b3caae5e7af2c30bbbfc3a4cb993c2c387813af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16641520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1163ff3ee0cced91b11c1885e3007fdc1fc42dca2de2ad55e338216325ae28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 22:50:43 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 01 Dec 2025 22:50:43 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 22:50:43 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 01 Dec 2025 22:50:43 GMT
ENV APIFIREWALL_VERSION=v0.9.4
# Mon, 01 Dec 2025 22:50:45 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='89c7d5ebcb35733c90b1adee529f7116adf7880311706029d2470af792176e0c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f8590efca3d526ea3b0a85b245bbdbb647bebcb01fcbc5bafeff03b81a479a70';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='90ac4e0c2b864e24e87b85f9012ff9c67ed5ae807828bc61ec4d5c6c30e6fabc';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 01 Dec 2025 22:50:45 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 01 Dec 2025 22:50:45 GMT
USER api-firewall
# Mon, 01 Dec 2025 22:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 22:50:45 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f70c60ef0bbe229a41d4d6bfacb0f0cea472a409b0442f3d8094d25857abfe5`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fad9856cbbaf6ef2fd95ba1ea5a37225d3b7901592d872f86ff0439aff5bcc`  
		Last Modified: Mon, 01 Dec 2025 22:51:11 GMT  
		Size: 12.5 MB (12502197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4bc2a3ea4af565986bb5e92c0b1b6d35b484e4549e03a45ee560d600e222ed`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2112c4e911ae873048340b999ce63635d9a4d35fd4e703d0042269130a315279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 KB (180618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6005ce27c628ac7875e9335475a0ebc0256de83a7d663cbc32e9fa535404bc`

```dockerfile
```

-	Layers:
	-	`sha256:aefdd50c3bbc9d11a7fc27ea0e862a1d9ecca4ab9e599e2294e0c39363393e83`  
		Last Modified: Tue, 02 Dec 2025 00:44:36 GMT  
		Size: 167.0 KB (167021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77da1addb1bb0e592824846a1414955241bf6f88ef6e09801aeeff502ff3a4ad`  
		Last Modified: Tue, 02 Dec 2025 00:44:37 GMT  
		Size: 13.6 KB (13597 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:b610b5a218bd353c0c0db2973caaad1f65a5cde3bc7a20ee9fa264820ed2d1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15674312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c01dd3a966341ee9395a421b9ed4609e9b4aa7ba57a67d76b41b19b049dff6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 01 Dec 2025 22:50:50 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 01 Dec 2025 22:50:50 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 22:50:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Mon, 01 Dec 2025 22:50:50 GMT
ENV APIFIREWALL_VERSION=v0.9.4
# Mon, 01 Dec 2025 22:50:52 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='89c7d5ebcb35733c90b1adee529f7116adf7880311706029d2470af792176e0c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f8590efca3d526ea3b0a85b245bbdbb647bebcb01fcbc5bafeff03b81a479a70';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='90ac4e0c2b864e24e87b85f9012ff9c67ed5ae807828bc61ec4d5c6c30e6fabc';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Mon, 01 Dec 2025 22:50:52 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Mon, 01 Dec 2025 22:50:52 GMT
USER api-firewall
# Mon, 01 Dec 2025 22:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 22:50:52 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da609a601a76b0fc61ac747b2ce4262b5a05dddbf491061e69010944542a7e60`  
		Last Modified: Mon, 01 Dec 2025 22:51:11 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b9a01ab00363fcc1624dd04b86cf34db0440700f630f09949493d79d9e45b2`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 12.1 MB (12054129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249addff1b82caaee61ffc39280ff27a01bf2128af5b85777e5d4d5398751e31`  
		Last Modified: Mon, 01 Dec 2025 22:51:11 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:4415fa2a3788c7670b8291a0a3d75d56584218ba6639ce73c6d984a78ee4cc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1a0fb3a53d2cd2a7a2fab74246ad54c87fe4790e537af8f6b5c4ebea305ce0`

```dockerfile
```

-	Layers:
	-	`sha256:7e33db088ab5d193f3014abc161b5ac547fb22308af7f0f0d352fc4ecbbfdfa3`  
		Last Modified: Tue, 02 Dec 2025 00:44:40 GMT  
		Size: 167.0 KB (166974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda890e8ff5752f5e00b250dba39b4b2a54b89fabc595c694b3786a19e8232d7`  
		Last Modified: Tue, 02 Dec 2025 00:44:41 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json
