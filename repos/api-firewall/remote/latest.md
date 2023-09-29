## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:f834d35d116bfb24afcdbdcf9c4bc8ac135e96caf5bc63170f0da428c00e0f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:fbc731e6e4f75228412fbe515ee2e9cf288b7b821c8fcb0d0b47fe2c370936ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13732339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76eeca7fb5bc787a3800ad1142254f5cd62141eb1954a962a79cc091c7c145c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:05:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 28 Sep 2023 23:05:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 23:05:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 28 Sep 2023 23:05:45 GMT
ENV APIFIREWALL_VERSION=v0.6.13
# Thu, 28 Sep 2023 23:05:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='42bc189c8302221d37eea69297a0edd8aa485f8856225019f4773bbbe72b4363';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='186e46d26eb64ccc10ea07b91fc7602cff5eba13f13ec5314222a65f991f8717';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='898eb09cae9b314f302be6fb27e6618428ded24cddc569fe8c37b27a02977657';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 28 Sep 2023 23:05:48 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 28 Sep 2023 23:05:48 GMT
USER api-firewall
# Thu, 28 Sep 2023 23:05:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:05:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d10d1b9bf91982a739d7bda21d63dbfed01ce2090d24e8faa4cd2833097d6`  
		Last Modified: Thu, 28 Sep 2023 23:06:02 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514cd8f75385dcb0dbcba8756d455f38ce54f988039055d2062fb5a6f526318a`  
		Last Modified: Thu, 28 Sep 2023 23:06:04 GMT  
		Size: 10.3 MB (10328812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e160cbd9145ad7e5262c2ea47f4956e0c495dcb1fce5595cc218d2e9b945c1c`  
		Last Modified: Thu, 28 Sep 2023 23:06:02 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:1b4930e2964ee9eb03a80cc3f34a0148d54f05270a4438dccaf227a8b8988aa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12916623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad27d9c913f449145c3bbbf1a125020680d7cc1b8d4540cf59373626ac4eeb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:15:00 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 29 Sep 2023 01:15:00 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Sep 2023 01:15:00 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 29 Sep 2023 01:15:00 GMT
ENV APIFIREWALL_VERSION=v0.6.13
# Fri, 29 Sep 2023 01:15:02 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='42bc189c8302221d37eea69297a0edd8aa485f8856225019f4773bbbe72b4363';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='186e46d26eb64ccc10ea07b91fc7602cff5eba13f13ec5314222a65f991f8717';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='898eb09cae9b314f302be6fb27e6618428ded24cddc569fe8c37b27a02977657';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 29 Sep 2023 01:15:02 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 29 Sep 2023 01:15:03 GMT
USER api-firewall
# Fri, 29 Sep 2023 01:15:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 01:15:03 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292281ca6fe77220b14c32e898bb9714dff247427c2e3b4596dfc7215d7d99c6`  
		Last Modified: Fri, 29 Sep 2023 01:15:16 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b48aa6b7e3cd77c9fb4bb92f1e9780f91d2b519a90ba11818fbc3e2355000e`  
		Last Modified: Fri, 29 Sep 2023 01:15:17 GMT  
		Size: 9.6 MB (9583235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5f44193a99084bdae22e97b02b86e37b2e9389b11ed803417bc60c87f1182b`  
		Last Modified: Fri, 29 Sep 2023 01:15:16 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:985c5476a5796a0c877475d689be13e5e11085fb0f954a149f438a7b64bb7b78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12229918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b11ad546836754b944d0331623808b0df7844f0b2d6cbfda64e5ad09041488e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2023 21:38:18 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 08 Sep 2023 21:38:18 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2023 21:38:19 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 08 Sep 2023 21:38:19 GMT
ENV APIFIREWALL_VERSION=v0.6.13
# Fri, 08 Sep 2023 21:38:21 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='42bc189c8302221d37eea69297a0edd8aa485f8856225019f4773bbbe72b4363';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='186e46d26eb64ccc10ea07b91fc7602cff5eba13f13ec5314222a65f991f8717';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='898eb09cae9b314f302be6fb27e6618428ded24cddc569fe8c37b27a02977657';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 08 Sep 2023 21:38:22 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 08 Sep 2023 21:38:22 GMT
USER api-firewall
# Fri, 08 Sep 2023 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2023 21:38:22 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810732c4c5731539752999614fb1453fcd5a97a7ddfc937d972268903995410e`  
		Last Modified: Fri, 08 Sep 2023 21:38:36 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a80848339d19fca5533c84901c1d184c734b59a42f334588c233b0f2b64cd56`  
		Last Modified: Fri, 08 Sep 2023 21:38:38 GMT  
		Size: 9.0 MB (8993216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7c9d79244812fe45486a3adc5053998ec5e22a579bb40dcb8ff2fa73e4161`  
		Last Modified: Fri, 08 Sep 2023 21:38:36 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
