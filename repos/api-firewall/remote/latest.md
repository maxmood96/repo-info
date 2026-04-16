## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d02812a69179a140b6213932d9fdc812c23ad823ddf9cecd0a41a49b4359269f
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
$ docker pull api-firewall@sha256:0b8f9609e50054ac715766652ad8781fe97f121d7ef2acdec0f20e854c3bd07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18496613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f563bf074cbb523479e7b442ddfd9c4fa770e38210ef49e678b5a2d9c48682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:12:04 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 15 Apr 2026 20:12:04 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:12:04 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 15 Apr 2026 20:12:04 GMT
ENV APIFIREWALL_VERSION=v0.9.6
# Wed, 15 Apr 2026 20:12:06 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c533716f7dd3db86a8b70879b83fe14292c8f5b9d3974daf20272317ac6e9ffc';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='274579a052a5ff966430ab279f5990a83839492817433f2ae5860abc0f4f7a5f';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='14ba27c545db203673269e02cf8c02edb06eddd71d6910f44e417a13a3ac664b';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 15 Apr 2026 20:12:06 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 15 Apr 2026 20:12:06 GMT
USER api-firewall
# Wed, 15 Apr 2026 20:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:12:06 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f9e1a8fab47d10b4948d7a161316f6eaab86105efd289e9eceab8e486a828d`  
		Last Modified: Wed, 15 Apr 2026 20:12:12 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e90028378bb7bf53493707d1a678cdb82423c898ac744495995bd1a0b3d737`  
		Last Modified: Wed, 15 Apr 2026 20:12:13 GMT  
		Size: 14.6 MB (14631177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6f20f69cf990949bdc2f83996f4d2e37a5fc734b2a90e7eca57b660aeb6156`  
		Last Modified: Wed, 15 Apr 2026 20:12:12 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:8194e1c8b8c0e29768d49fc25ed6adf51718342f6e06cb0a41fe6fd03606804e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 KB (184145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfe554cbeabde350a753f5e409f995d72c07a40994c7b7d1d814e976af97c8e`

```dockerfile
```

-	Layers:
	-	`sha256:7d5d2cf68ea32e8e0e1fb9c7b77b5c18d6a688ce49948e6268b1b26d1667daf3`  
		Last Modified: Wed, 15 Apr 2026 20:12:12 GMT  
		Size: 170.6 KB (170642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa33cad705358daf00288043c90faa1ceea995f58a0fb4d85d93e4128c85bf08`  
		Last Modified: Wed, 15 Apr 2026 20:12:12 GMT  
		Size: 13.5 KB (13503 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:1ffc141cde6ff3974b9a1458f72f84a60acf1f146cafb88f54400bf9ea2f7418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17514491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f11690421427c4a47b544ab585d6446126d2ec3f614df80b76395b0fe56c6a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:55 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 15 Apr 2026 20:11:55 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:11:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 15 Apr 2026 20:11:55 GMT
ENV APIFIREWALL_VERSION=v0.9.6
# Wed, 15 Apr 2026 20:11:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c533716f7dd3db86a8b70879b83fe14292c8f5b9d3974daf20272317ac6e9ffc';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='274579a052a5ff966430ab279f5990a83839492817433f2ae5860abc0f4f7a5f';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='14ba27c545db203673269e02cf8c02edb06eddd71d6910f44e417a13a3ac664b';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 15 Apr 2026 20:11:57 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 15 Apr 2026 20:11:57 GMT
USER api-firewall
# Wed, 15 Apr 2026 20:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:57 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8295977f12f1b671fb8928097fcf94ed5b54ac958e42ed554619e2aefff4ba`  
		Last Modified: Wed, 15 Apr 2026 20:12:02 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8835f86486dd452d45a2a48fd1b7131cfd44b30bc611fc02bbdb0319a188b13c`  
		Last Modified: Wed, 15 Apr 2026 20:12:03 GMT  
		Size: 13.3 MB (13313371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d073d59e3edf5d2b0b17ea7239be41c081ea71a61f9c03a6df597450be1310`  
		Last Modified: Wed, 15 Apr 2026 20:12:03 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:366f8715ef83604b0b7c09dfe8479885f9fdef121394a9563948409723749f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 KB (183622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc5d3ca712cce05c82d8eaf6e1c641c96df49432d2617b1dfd337c7e3f01bd3`

```dockerfile
```

-	Layers:
	-	`sha256:b22244010a7d6cecc9c469307f3b5fc6e06adf4c395b02d47a703f4a87a2cf84`  
		Last Modified: Wed, 15 Apr 2026 20:12:03 GMT  
		Size: 170.0 KB (170024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d4fb63b9331ec32c782bf28ed51547b191887559dcc5bcad98994d5041d619`  
		Last Modified: Wed, 15 Apr 2026 20:12:02 GMT  
		Size: 13.6 KB (13598 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:f5d955c7e900a409b59e7e581727164f75c53974c66566df492bf9c804bd58d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16717651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d00818b23b6d3e5ccaa316a339fe25aebae1426616a398ee7a15043757dff12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:19:26 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 15 Apr 2026 22:19:26 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:26 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 15 Apr 2026 22:19:26 GMT
ENV APIFIREWALL_VERSION=v0.9.6
# Wed, 15 Apr 2026 22:19:28 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c533716f7dd3db86a8b70879b83fe14292c8f5b9d3974daf20272317ac6e9ffc';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='274579a052a5ff966430ab279f5990a83839492817433f2ae5860abc0f4f7a5f';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='14ba27c545db203673269e02cf8c02edb06eddd71d6910f44e417a13a3ac664b';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 15 Apr 2026 22:19:28 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 15 Apr 2026 22:19:28 GMT
USER api-firewall
# Wed, 15 Apr 2026 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:19:28 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03f30290c8d817df3099a25a8c2bad937f0fc2d867cbbdbb400fc7e184563a`  
		Last Modified: Wed, 15 Apr 2026 22:19:34 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79fab73035705774d017f8333fe91220824ca51a529a4561c1f342d82ab0cef`  
		Last Modified: Wed, 15 Apr 2026 22:19:35 GMT  
		Size: 13.0 MB (13025957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e49f7d38c24c1dcae6692473f440201b85fd34c0ffc17dfee9baf61da56f21`  
		Last Modified: Wed, 15 Apr 2026 22:19:34 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:d3a5b57fce2004d0f0e05e46e6ac4626518fc3e7db03036f748f1061368cca16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 KB (184104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c354682c226434ecd57ba414b2a27111bde18183236abf4d6827bf354b28ab90`

```dockerfile
```

-	Layers:
	-	`sha256:6d249737b5fa6733058f5011a9427e34882fccf0ce59ef802779f4b0162f22ea`  
		Last Modified: Wed, 15 Apr 2026 22:19:34 GMT  
		Size: 170.6 KB (170627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b53e977af62b95ad47741075e7f42713e11080e2d5e5267a8284704a4288e0d`  
		Last Modified: Wed, 15 Apr 2026 22:19:34 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json
