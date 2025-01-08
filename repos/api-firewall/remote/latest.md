## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d7a2d4e8d03d1a87eef6742843dcf2f088a55c4c82c56cfe6bd2db01cde6be62
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
$ docker pull api-firewall@sha256:95b51573cc0b2d1aea11dcab1c3a9c7c373279a308d3717fa7f21d09193fa4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2556ddbb833cdc0f41e1934fb6f4f9f7cd3c593bf9f92b2705d1d8356f198a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f493e165054334fe502f4c9168686cfb797bddfa179d18c0bd51853321cf37b8`  
		Last Modified: Tue, 07 Jan 2025 03:13:43 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ff132dd362d4fbef9f595c5919bb74ff8a1e25ca90bf8edd59de2bfac53a3a`  
		Last Modified: Tue, 07 Jan 2025 03:13:43 GMT  
		Size: 11.2 MB (11228339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2539153e486786626103553aa0abf54206e669205eebdc0c9578a52ce963a91`  
		Last Modified: Tue, 07 Jan 2025 03:13:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:13139d84a35f1e13f7404b05d018ad33c11df2c020f1bc9f988cce0bb5efd064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (157955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd26278ec968a11dc6fc47244c4e98772ea6f2f5346db9019b97a99342c9a72f`

```dockerfile
```

-	Layers:
	-	`sha256:9fc0c8fa74edf6d79a41e4c2241ba8a62be497621b50b76aa69063ea3cc2001d`  
		Last Modified: Tue, 07 Jan 2025 03:13:43 GMT  
		Size: 144.4 KB (144409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b965a2704f6414f7c186d7a41db565da2f91e579c847c0a4bb7057878237be7`  
		Last Modified: Tue, 07 Jan 2025 03:13:43 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:1f3a04dd2e2413d2ce1485cda56d89e0cf857bf5786215025327cb0b85842dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14342603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c4f301970469e093039cebce758d9f645a7a1938ee65423a23b085d04e05e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0470619f19d7b542810d65ef73b7720b410f3dc7d55785e8372759b543445e`  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e56f47d35eb86095dc1afe5d7ec22d184c61bcf12cff62a08ab9cc5901a46`  
		Last Modified: Tue, 07 Jan 2025 03:42:22 GMT  
		Size: 10.4 MB (10358333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034c5f800702dae01720e0ac9f6571afa546ad071f49414c8a6dd58d13db837c`  
		Last Modified: Tue, 07 Jan 2025 03:42:21 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:b7699dd7d397aaddecdf6200e65dbe24627fd2c012d68a194f1375bfcc6a4bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4bd285cdbb01c0f20c94af726a2c1e01fa79c14036fc9113f745a0b2c6599f`

```dockerfile
```

-	Layers:
	-	`sha256:0be2fd290f9ba0ae5d0a2c0990e2c3962c62ecda70506b86212ed93bb11d4f41`  
		Last Modified: Tue, 07 Jan 2025 03:42:21 GMT  
		Size: 144.4 KB (144441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec28c0d12e42fb8fa872a6c8faa021ca1308dd142505d067a20ce926a39a61dd`  
		Last Modified: Tue, 07 Jan 2025 03:42:21 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:875fba8efbbf8780cecdcb6aad8ba0d351e88a57fbae67dddc03bf097605cbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13191511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7e309f6da6d469be43eac151c80ba154fa8cfbaa418b5d828297fe5fa90990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c9157f234faaf9af1491ed50a17435f09bf85bf51071f6e0502661e45f85f`  
		Last Modified: Tue, 07 Jan 2025 03:13:57 GMT  
		Size: 905.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a02f8ba93f39d998ba77f929fc07b34c4c366db8f53844a68987eed4d7f53`  
		Last Modified: Tue, 07 Jan 2025 03:13:58 GMT  
		Size: 9.7 MB (9731984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a753c8c38f8b93cbba9cfd458f38f4801d3f0ec5685318a6167dce016ef0d8fb`  
		Last Modified: Tue, 07 Jan 2025 03:13:57 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:2041d2c16d0508247dd7b32ad91e8af367ef6001d2a0a96a08f5410b08af38e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 KB (157914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf8522c78170bc02dc81133c3d38f0f098393021d4db3ba0c65b84c7b68ac0`

```dockerfile
```

-	Layers:
	-	`sha256:022bf153a187650ed4dd8a89ae2aaefac3a846b004e35599b3e6af9bb7dae918`  
		Last Modified: Tue, 07 Jan 2025 03:13:57 GMT  
		Size: 144.4 KB (144394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940834aa3b398f6eded584e2caa33de6da2c42c3309e55482e3f8f0b0843bf59`  
		Last Modified: Tue, 07 Jan 2025 03:13:57 GMT  
		Size: 13.5 KB (13520 bytes)  
		MIME: application/vnd.in-toto+json
