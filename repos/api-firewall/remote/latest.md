## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:2ec63705362c74a1cef64bb859ea1bca6beba15b415a3764024ace6ad46a6dec
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
$ docker pull api-firewall@sha256:606bd91e8f8c3920a1cba91ba7dc3c4398774f2a9245912b591721ebf7c610df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14874040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626ad0c0dedff3f60dbcd17db4a6608dab5982987c7feaf8dcbcd55f97434d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3e4d2c270245e9a590e4cacd67a19370228870792cd62f4091f41cc78ea0b6`  
		Last Modified: Fri, 20 Dec 2024 21:28:27 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f95eb265d1ea2eadab97e2acf01b59bdd041cc13d8c01bf5eb6d6b8a534b0a`  
		Last Modified: Fri, 20 Dec 2024 21:28:27 GMT  
		Size: 11.2 MB (11228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceabbdefd227bee6e40bfeac774ec6e01d6a764aae434ded1575a9f741cfb539`  
		Last Modified: Fri, 20 Dec 2024 21:28:27 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:53bda069fd9f4aa12cb260e13896a4280aa2a33f95d58ccfe805acd0fc39d769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (157955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963a4fd1520fc1839db21d23a467a64ff50080e756b247b16bf406e1b5ea8caa`

```dockerfile
```

-	Layers:
	-	`sha256:cd13ed25467d6bdd2daac59719796b549aa2ec49e60cd37e3de3587dc8c92aec`  
		Last Modified: Fri, 20 Dec 2024 21:28:27 GMT  
		Size: 144.4 KB (144409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb3a4890602403c7846a58024087741cd5af22bd9b5892860935ca482245072`  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:1db1a23dca8a40873682a41e030358282fb15eb617d1b4a6ff02192f20b0f1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14352758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f464bce7564fec82a5e581c26282c821191db99060d9d737baa0d4b6674af52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6c7c1b3c655bc0ac115c21f5c5c84fc654ad073f8e3f33298ca064b4539a7`  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec65af62ccf999456b7b4ae75707ceac48697c1b9f9e777dfd329d47c8ef4d0`  
		Size: 10.4 MB (10358307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b518cfb71f33e72e753b225f15ad86adf605989552f59ca19cc04a63463bb83`  
		Last Modified: Fri, 20 Dec 2024 21:33:22 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:f2c8733c36b1ee6a168001db8c104fb62b0ac9456479b06e5fd7eeb2fdbc1e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bca9a2a5067bae84db598a51da275092701471ce89527b1b360bcc4d6ad399`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7d40d6f5818bc1dca8337bfbb6372e9c90d3f4ee7c87b7878d281ebbec388`  
		Last Modified: Fri, 20 Dec 2024 21:33:22 GMT  
		Size: 144.4 KB (144441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f683df3cb183078e5d2f897c4f55cfe29e87292081eb1c3d67e509d9a1237aec`  
		Last Modified: Fri, 20 Dec 2024 21:33:21 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:782a4f9854e5654ed40e8a338c500b624b15ae1fe7144bfa6b87b478f26c4843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13199304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a8276c9d36143d323003262fd35bafab7b80f8f67049daa930d333e6b5b51e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f220be47da6f10c62d62b7b3eb9ef34a55ad4d7733b4d6cabed89d5bf7393ac`  
		Last Modified: Fri, 20 Dec 2024 21:28:51 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f17ed9368d15389d8f0d3b1b2f48703331fc7d36f761d78b6a15454a4e90cc7`  
		Last Modified: Fri, 20 Dec 2024 21:28:51 GMT  
		Size: 9.7 MB (9731960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fa24a1b59111f00e98739a080e827ba7f5847d774abf11b9166c3dafba7e0e`  
		Last Modified: Fri, 20 Dec 2024 21:28:51 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:1ced8cadf6d3bdf9f194b6f6642b6608f51cecc6f38836a579a9783c081b1509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 KB (157913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e559db765300c0aa1d22e375c4c644282e7f6d16f763dbf0a3a3aa938537963`

```dockerfile
```

-	Layers:
	-	`sha256:73368c000676a2f36d6231dc6b6aad757b8c38952fb41f865b732f92e2d32f66`  
		Last Modified: Fri, 20 Dec 2024 21:28:51 GMT  
		Size: 144.4 KB (144394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a199389dc16fb9b9c6915caf0c89c39d20a370a48fe413d695b752370267f5c`  
		Size: 13.5 KB (13519 bytes)  
		MIME: application/vnd.in-toto+json
