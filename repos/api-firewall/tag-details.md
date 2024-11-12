<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.8.4`](#api-firewall084)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.8.4`

```console
$ docker pull api-firewall@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d24338e4a04afc6ef9672ff9c14d751de8906b1e7f5ef002d7ea54dce8528cba
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
$ docker pull api-firewall@sha256:01fb76bc8a537ccbde8c5ac3506ca1ef56b87dea62f5ec1679cac5db5e28ab20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14855650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38ef4f594d69001b5d6e04419a192634180da0e8dd9a21a3d106484989b76bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29705d787ea2178ce6821332fed21c9b4929a5e9db00501d59921564b56caa49`  
		Last Modified: Tue, 12 Nov 2024 02:01:17 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682864540b327d2590879461e609829fcc3ec2c5e45ec3aae43d6b58343c4bfc`  
		Last Modified: Tue, 12 Nov 2024 02:01:18 GMT  
		Size: 11.2 MB (11230484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cf25d132c5f96dc493be41df80acb7ef995cc72317f072efdc1c938720f10`  
		Last Modified: Tue, 12 Nov 2024 02:01:18 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:430eff868c6cf861b24838acb46d139757ac837a170deae9fb9f9f894889d62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2122a2c8c72d49fbbe288060f617bf8f02bb354cd7a286cb4c59bd1299e3a4`

```dockerfile
```

-	Layers:
	-	`sha256:12ea658ad0b9c9c5a2a208535cf043eedfb3f754ff8faa2135a648e5756b5a18`  
		Last Modified: Tue, 12 Nov 2024 02:01:17 GMT  
		Size: 13.3 KB (13331 bytes)  
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
$ docker pull api-firewall@sha256:c44dacd5247dd4cc661739427a1a71ecba6b37216890c780193e5f75679c503a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13219808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103b6752cb1f0641229f3b348b7ecae70bb9cc0b67377cbeca2c5e08b166adf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c06b599149ec5199f9e563a91012d2e5e3540a8483329e034b5ed5c67690321`  
		Last Modified: Tue, 12 Nov 2024 02:01:25 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f50f59ff5aa9ef8de0fc0eed4d98ccc6c819e5b50e7e66ce852ee05448ada0`  
		Last Modified: Tue, 12 Nov 2024 02:01:26 GMT  
		Size: 9.7 MB (9749325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b495c6c16242cad7426cf81f1e6d748ab7177149c1b25821e77f20f50705cd6`  
		Last Modified: Tue, 12 Nov 2024 02:01:25 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:84ebf540cbbe0fec183b9185e81643cd8cacf4a723f0e8d4828b1938a57074cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0681b70556d710d0675402cdbf1ca68b95c7ccefad8e6b35351d4733652d2bdd`

```dockerfile
```

-	Layers:
	-	`sha256:d8a9223c536f8b07d1fcb1098c4d3fcb3ef568ed7ff413bb83c81e808afac37a`  
		Last Modified: Tue, 12 Nov 2024 02:01:25 GMT  
		Size: 13.3 KB (13305 bytes)  
		MIME: application/vnd.in-toto+json
