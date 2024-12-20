<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.8.6`](#api-firewall086)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.8.6`

**does not exist** (yet?)

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:5221dd62ac114389f235f6220fae0cd526293342783d66bb8b5e4def14bd80bc
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
$ docker pull api-firewall@sha256:d48536ca0d011c81ac776beeb610d8b308d406a97986dfd57b5e616a4a8bd0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14874135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ab98ee89b5d9713e454b48aa61ed084c10d63f98b807c20854f4a9e7320c65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 18:20:58 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 13 Dec 2024 18:20:58 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 18:20:58 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
ENV APIFIREWALL_VERSION=v0.8.5
# Fri, 13 Dec 2024 18:20:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb78d1ec8487d8bdda99f48be1da32d1ca57f47a57d51a14f881f2a1f17e777f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='e0334cc6df7e2c9a281c43bd039525e2479fddf835029dc981b18f404586f370';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='76528b49cf9530aa45f294115d2dff86c6722a68fc2e3beb3ec173095eed6b9a';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
USER api-firewall
# Fri, 13 Dec 2024 18:20:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 18:20:58 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326465bfc32f2b16921b54752060b926c6a81287fd9cc233d6138bf96522f075`  
		Last Modified: Fri, 13 Dec 2024 23:29:27 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc8af469d4759c3544053ee1a4966003da313a6732ae0a384387e1411d70096`  
		Last Modified: Fri, 13 Dec 2024 23:29:28 GMT  
		Size: 11.2 MB (11228431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a4978866a8f4f479102e440463ca1e7a9b9ae50ac8df481479b97a6d200d00`  
		Last Modified: Fri, 13 Dec 2024 23:29:27 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:628a59936498995f1f8fe248364a03ffb778ee9e763238d4d9fcb31557da7615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f525cc8126ce9bc5e6a987bc1e329d1c22bdafbdf29fb70c1e89acf3cbe57c4e`

```dockerfile
```

-	Layers:
	-	`sha256:21f0d8bc84c89eec89ed98a4f917295753002aa28d559b79dd9aa77f48c3b5c5`  
		Last Modified: Fri, 13 Dec 2024 23:29:27 GMT  
		Size: 13.3 KB (13331 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:9eae5c35cbbc63781cd386ea75055019c158029d2cdbd83211a7c53f8c6bcb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14352637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af840b7d8041a6c753f5700aac67a6d27e12ce33f08f7fc6d15fcd75b965d7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 18:20:58 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 13 Dec 2024 18:20:58 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 18:20:58 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
ENV APIFIREWALL_VERSION=v0.8.5
# Fri, 13 Dec 2024 18:20:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb78d1ec8487d8bdda99f48be1da32d1ca57f47a57d51a14f881f2a1f17e777f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='e0334cc6df7e2c9a281c43bd039525e2479fddf835029dc981b18f404586f370';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='76528b49cf9530aa45f294115d2dff86c6722a68fc2e3beb3ec173095eed6b9a';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
USER api-firewall
# Fri, 13 Dec 2024 18:20:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 18:20:58 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50394cb2d43cfd89f10c46ba15371a60b9717d01b4a3633c2f8c1e0a1ce8d9bb`  
		Last Modified: Fri, 13 Dec 2024 23:26:32 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a02d3571f06af1edd3e345ec4bcd428d014d5d55477fe5d952f0172b6d46a83`  
		Last Modified: Fri, 13 Dec 2024 23:26:33 GMT  
		Size: 10.4 MB (10358191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e5ba5eaa2279fe6a3e47d6984c7d8fff191179defd6f023e0b2b05a4a2dcf`  
		Last Modified: Fri, 13 Dec 2024 23:26:32 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:3d5e0741c3e4060b9ac84dfa5c853b2580109db322dbaf295bc3f74ccf41db13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d75798756aa07944f2a7b395638b6318abfa2e6f33c6a96683f3564acde83d8`

```dockerfile
```

-	Layers:
	-	`sha256:8ce5b0c52719a476a63d35e8164030f4c2256ee6a0a651c3a546d6515d4becab`  
		Last Modified: Fri, 13 Dec 2024 23:26:32 GMT  
		Size: 13.4 KB (13426 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:338c81952ae830c3d71795a9b5d6807384dce7b1f44895f9af9712bafb35093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13199248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0dee1d0cf55bb820588065fe3c9451b8bcbd71934311ed8e7f8ef1238488bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 18:20:58 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 13 Dec 2024 18:20:58 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 18:20:58 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
ENV APIFIREWALL_VERSION=v0.8.5
# Fri, 13 Dec 2024 18:20:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='fb78d1ec8487d8bdda99f48be1da32d1ca57f47a57d51a14f881f2a1f17e777f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='e0334cc6df7e2c9a281c43bd039525e2479fddf835029dc981b18f404586f370';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='76528b49cf9530aa45f294115d2dff86c6722a68fc2e3beb3ec173095eed6b9a';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 13 Dec 2024 18:20:58 GMT
USER api-firewall
# Fri, 13 Dec 2024 18:20:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 18:20:58 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968a8a34ef4cba82354921c8d0007480526f9a02500f39c17229b5a7352535a`  
		Last Modified: Fri, 13 Dec 2024 23:29:27 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db336c4bc5fca2eb035735c733b6c8ccb83a8193b7c5e2b2e397ae8b3a04b887`  
		Last Modified: Fri, 13 Dec 2024 23:29:28 GMT  
		Size: 9.7 MB (9731906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa72b65eb9b379c12fd6a79a674fcb7e129a7a71827bf1c64190362d735a59b`  
		Last Modified: Fri, 13 Dec 2024 23:29:27 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:b94a44cf169703ff45a154dbeb53f8b2eab8a03354c4ece41250385ab9cbd1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ad4773540292f2a4d1a84e7ca16241b1caa88b2b1744fa5930a93e7d4b7b45`

```dockerfile
```

-	Layers:
	-	`sha256:29b57686b4ef5233a368b797096005a1b76eb1d2f55633422837411fc6666bfa`  
		Last Modified: Fri, 13 Dec 2024 23:29:27 GMT  
		Size: 13.3 KB (13305 bytes)  
		MIME: application/vnd.in-toto+json
