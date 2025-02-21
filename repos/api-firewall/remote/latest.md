## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:160dcbe5f16048c4091e0832d89f20d9613eadb73b7405c1c808915284904112
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
$ docker pull api-firewall@sha256:39be85572cc29b2738a542675298d57cfe2890d6b107aeaac00b849e37449a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14871851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6236f59b4fec1d13696b48820ddce4f9b25c2a06528a273621ea65ca4f96bfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 14:14:14 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 20 Dec 2024 14:14:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Dec 2024 14:14:14 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
ENV APIFIREWALL_VERSION=v0.8.6
# Fri, 20 Dec 2024 14:14:14 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='097a1d0ae22e50a25907e1817e602c7799bc372207f92fc7e72b58f9124b4e9a';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='5eb8e46690991f41d09160c28de2185c7f4cf8bcbe3133f89c8ed7b0cef7d2ff';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e752a19f95312accfa8946ae3095340c143ecbfb3380489b6a7b0b3466e95613';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
USER api-firewall
# Fri, 20 Dec 2024 14:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 14:14:14 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e456b3d73cea286734188a9aa362425f07cde4db4f1783e35fe672c1fccb2b98`  
		Last Modified: Fri, 14 Feb 2025 19:10:34 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a9a812d64ee1a2b47961309b8c545fa412e8f5ee53ddeb2f7a89c29e022ad`  
		Last Modified: Fri, 14 Feb 2025 19:10:35 GMT  
		Size: 11.2 MB (11228355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece295bc6e398369406986689b4c2aaab132fe23810bb1152446337af6b2cd60`  
		Last Modified: Fri, 14 Feb 2025 19:10:34 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:72ff7f9813c955cda492f9d357b46a0f6455b603c2575038174c433b9afb70af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (157960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6be292c23e479b5825791ae8e6652c4884807bc25d914714ea0b402aaa06615`

```dockerfile
```

-	Layers:
	-	`sha256:361228fd77fa34aa94b9808e9234b1852e3a255c82cedc159294709569adf302`  
		Last Modified: Fri, 14 Feb 2025 19:10:34 GMT  
		Size: 144.4 KB (144415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14843954ceb91ec3b7cd364b5e39f0dcc1235b295823e728cdaf40f8da6e85db`  
		Last Modified: Fri, 14 Feb 2025 19:10:34 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:bd4ed2d161f7df5697dd03b66618078ec521e0c7278c91927d1bbe52a34397fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14352618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc2408bfa7a26d03cc846965ecdba13984cb3bb2e84777bb8c7fc2d2a85440d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 14:14:14 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 20 Dec 2024 14:14:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Dec 2024 14:14:14 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
ENV APIFIREWALL_VERSION=v0.8.6
# Fri, 20 Dec 2024 14:14:14 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='097a1d0ae22e50a25907e1817e602c7799bc372207f92fc7e72b58f9124b4e9a';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='5eb8e46690991f41d09160c28de2185c7f4cf8bcbe3133f89c8ed7b0cef7d2ff';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e752a19f95312accfa8946ae3095340c143ecbfb3380489b6a7b0b3466e95613';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
USER api-firewall
# Fri, 20 Dec 2024 14:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 14:14:14 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d69a531d9b48db67cfa76d5aa44d86ce1128f0c625da3819f211af26fa5201`  
		Last Modified: Fri, 14 Feb 2025 19:13:46 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4842e0a3e744067b5bca240cd52207aea30cddaa971ded4e0d05e04ab8279bb4`  
		Last Modified: Fri, 14 Feb 2025 19:13:48 GMT  
		Size: 10.4 MB (10358341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adfed7c7fcf4d6eb9be9688c3a03d9591f8872a9fd5b53acf537a584cc6bc3d`  
		Last Modified: Fri, 14 Feb 2025 19:13:46 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:92bb003b5a80d38126577f189d308dffe86bf1cb2a3e0ffe25d9fede0a0f6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5c0545f5879f377f5e295b81cc4cd802d9ddda9ceb84065005349e5e6db33d`

```dockerfile
```

-	Layers:
	-	`sha256:bc84907246adf33e39fdcaf33d31285165a4c53d14256dfbce4c823b07f1e466`  
		Last Modified: Fri, 14 Feb 2025 19:13:46 GMT  
		Size: 144.4 KB (144447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30e09accc274b2c1062bf7d4dc070b27eb72d33c0fe80364bd75173b762f9c4c`  
		Last Modified: Fri, 14 Feb 2025 19:13:46 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:e387ee447f61ac000854837eb179594a1c69856de050daee89968183273acf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13196809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014b9f672a193dc15c36f6ca528b58043e56d9dda00938c0d0a13e7d36771b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 14:14:14 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 20 Dec 2024 14:14:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Dec 2024 14:14:14 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
ENV APIFIREWALL_VERSION=v0.8.6
# Fri, 20 Dec 2024 14:14:14 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='097a1d0ae22e50a25907e1817e602c7799bc372207f92fc7e72b58f9124b4e9a';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='5eb8e46690991f41d09160c28de2185c7f4cf8bcbe3133f89c8ed7b0cef7d2ff';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e752a19f95312accfa8946ae3095340c143ecbfb3380489b6a7b0b3466e95613';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 20 Dec 2024 14:14:14 GMT
USER api-firewall
# Fri, 20 Dec 2024 14:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 14:14:14 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915c7eb8a38abc8b2962929d6181fc7faf51b97d25c1a4bd3155f10c0707199a`  
		Last Modified: Fri, 14 Feb 2025 19:11:11 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065534ca4b4eea531798bc6a94d5a09c655ac9e8548ef8e9f908cf1bd9f0207b`  
		Last Modified: Fri, 14 Feb 2025 19:11:12 GMT  
		Size: 9.7 MB (9731933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904db2f6df610ed875c8e0495dad96a3e2421ee25f7cb8e88d5bdfa1d983c7c2`  
		Last Modified: Fri, 14 Feb 2025 19:11:11 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2ac69790887381b58bea654ae03b0fe778b17aa497c1ade843cd7d6698e1dc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 KB (157920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a23dc9c5199e34cb7cd814d9a2e206380c9578aaae7c8536481be2be0eb8fb6`

```dockerfile
```

-	Layers:
	-	`sha256:c0a08a7811faf54f3167e8765cff19b4260691404020e98a711f1a4345e67a91`  
		Last Modified: Fri, 14 Feb 2025 19:11:12 GMT  
		Size: 144.4 KB (144400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1195fdbfdbe80bbd0490e14b41b5c3a81f83ba7a88d71c41f2de2025c62c1d0d`  
		Last Modified: Fri, 14 Feb 2025 19:11:12 GMT  
		Size: 13.5 KB (13520 bytes)  
		MIME: application/vnd.in-toto+json
