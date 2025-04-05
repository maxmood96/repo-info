## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:d77e306d7b802358c67020cacdde42d78ef7a4ddb0bdbea9217d4d275442a037
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
$ docker pull api-firewall@sha256:c5977043a9ef4841e380548da47584a7e73d0bf1ef69ec8ecc5b6038563c4bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16375236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98d120d74ba8cfaf6b60fc44a13547e18dbd3d0927f5a3b2540e79078deae5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 19:06:57 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 04 Apr 2025 19:06:57 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 19:06:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
ENV APIFIREWALL_VERSION=v0.9.0
# Fri, 04 Apr 2025 19:06:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a06c49da96ac92bc85c0d318201cfc6fbf76bff08c3d807b61e5f4aa287f3a63';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='241d4322ca409141eb6a48aeca3828c67d37046624502326694e77e9e621e0b6';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='2dc58efdc21a32332b6edea2e732f1ce6571aa96f976d659202d872fb295f358';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
USER api-firewall
# Fri, 04 Apr 2025 19:06:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 19:06:57 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e609397cf305f9171a59420bdd19ce2eee372ed9081f3915f4225dc38ee430d3`  
		Last Modified: Fri, 04 Apr 2025 20:35:34 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60202f25b8e1f714684219352522f573040570d11f9dafabf7c89dc749169fa1`  
		Last Modified: Fri, 04 Apr 2025 20:35:35 GMT  
		Size: 12.7 MB (12731740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5bf780eb0151f95466d0d91ab37e91c6bbcb5d1f3377f8c78d50c636ad308`  
		Last Modified: Fri, 04 Apr 2025 20:35:34 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:79f6930968fc521b9f41e35c5893f9ef13ce17c31453e2436c55543899fc2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 KB (170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fced1a76e6cb4006e7575bfe953e5a8afbf51bdebe23de4c90fad944ad8ef1`

```dockerfile
```

-	Layers:
	-	`sha256:584add032cd1bd643f4bb33252987421ef9fa2c83d39f83736641275b4fbbffa`  
		Last Modified: Fri, 04 Apr 2025 20:35:35 GMT  
		Size: 157.3 KB (157312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f593da47f04f8bb6662bd15636f81823a089dc9247dab7dfa69e4d469d2bf5`  
		Last Modified: Fri, 04 Apr 2025 20:35:35 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:197c230d538214be163bc19ccff491910688fff18aaa6af3c3b7bcd4f3c1fce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15731387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cb7da71fa06981caca7ec94fc018644b52f96f4fbf9db7081d31a695b77e21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 19:06:57 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 04 Apr 2025 19:06:57 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 19:06:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
ENV APIFIREWALL_VERSION=v0.9.0
# Fri, 04 Apr 2025 19:06:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a06c49da96ac92bc85c0d318201cfc6fbf76bff08c3d807b61e5f4aa287f3a63';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='241d4322ca409141eb6a48aeca3828c67d37046624502326694e77e9e621e0b6';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='2dc58efdc21a32332b6edea2e732f1ce6571aa96f976d659202d872fb295f358';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
USER api-firewall
# Fri, 04 Apr 2025 19:06:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 19:06:57 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b04aaa1e648bcb03e0a94361d4b53e7feedbd930bc870214eca4adfe1b56b70`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0d759abf55da9b9ede8525cdba2b4ff34c7bcf2be561c647b7610eaffc523d`  
		Last Modified: Fri, 04 Apr 2025 20:35:11 GMT  
		Size: 11.7 MB (11737114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b230b8ee35eaf248ee7df4509fbd84ffb0df95150c5c67ed400a1a59b662a8e`  
		Last Modified: Fri, 04 Apr 2025 20:35:10 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:ff0d0c38211e371296efeabf62c23b7dd423c49517be0e9f76c5c5b4cffdb9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 KB (170985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b19817104b349088506aef3e585d9382e70ab56090a6cfd641926388a58b67`

```dockerfile
```

-	Layers:
	-	`sha256:85c4a5e2156b381a608b406837b8fb3dfb7b154d9d2c54eb1f008b54122c54d1`  
		Last Modified: Fri, 04 Apr 2025 20:35:10 GMT  
		Size: 157.3 KB (157344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c285e6b6daac8b9d270f7685dd81d07d919db53ae495d227e1e9d51a69a393e3`  
		Last Modified: Fri, 04 Apr 2025 20:35:10 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:23c851e7046690d8325a45b9ba680bd5b5a0e802ec10d932098b86d97e351e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14631838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5fedef03e0ad4248448e74416ea660995b32f43d32b24d84d5af5db2f29684`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 19:06:57 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 04 Apr 2025 19:06:57 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 19:06:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
ENV APIFIREWALL_VERSION=v0.9.0
# Fri, 04 Apr 2025 19:06:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a06c49da96ac92bc85c0d318201cfc6fbf76bff08c3d807b61e5f4aa287f3a63';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='241d4322ca409141eb6a48aeca3828c67d37046624502326694e77e9e621e0b6';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='2dc58efdc21a32332b6edea2e732f1ce6571aa96f976d659202d872fb295f358';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 04 Apr 2025 19:06:57 GMT
USER api-firewall
# Fri, 04 Apr 2025 19:06:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 19:06:57 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1b74465c926e28d20f135d3717900a411279ae7c9f19bb7543b24847d94b35`  
		Last Modified: Fri, 04 Apr 2025 20:38:04 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0c9350bd9d72a4500f16843aee1ec1b636344e17178236aa2d2700f1226a87`  
		Last Modified: Fri, 04 Apr 2025 20:38:05 GMT  
		Size: 11.2 MB (11166964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68d4d73c9f0fcc032f25ef40a83941c73b3a279efcbdcc157ed690af0fd477`  
		Last Modified: Fri, 04 Apr 2025 20:38:04 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:4b3c269b7ec50bfd8b452dcbb6b0f58d5c4dd165ade5aae4bd2849523a9a3234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 KB (170819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc09978d2bfa45d38b047c3ed66a6928ef073846f713ee15c456f1d30707e10`

```dockerfile
```

-	Layers:
	-	`sha256:4bf456cdd57f229d30527e5303ecc9967e1402fb861db5da6031dc985dcd2843`  
		Last Modified: Fri, 04 Apr 2025 20:38:04 GMT  
		Size: 157.3 KB (157297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf87f7cf8f5d2e698a1323e365228ba97e249646c9ce287cbce3be65c7006bd7`  
		Last Modified: Fri, 04 Apr 2025 20:38:04 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json
