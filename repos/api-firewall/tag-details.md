<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.1`](#api-firewall091)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.1`

```console
$ docker pull api-firewall@sha256:be771f0ac41500b1db84c7aa5773f7e44bf7ac53aa0fe42ed63d759ec15e0d03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.9.1` - linux; amd64

```console
$ docker pull api-firewall@sha256:adc2e53fd6bf37ab18766bde17f72da1d83ee109b0ee1388629bfd4f0d0abb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16378778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7522389418bd410eaf0586d52cd05a374f8d2162315bd51059fa48c2da06a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd98c535a67674bd4022b684a1389cdd494562ae9ef6489321c54ff5c8b7b0`  
		Last Modified: Sat, 17 May 2025 08:30:47 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094363e0132e2f4d62d846596c6b692992e5eb918141b7336e2dea5b8ca0d49d`  
		Last Modified: Sat, 17 May 2025 08:30:47 GMT  
		Size: 12.7 MB (12735277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819981fe71ee9f7f73ddc8cb1ea55748e61c34ac63550cd35a211524f2ed3083`  
		Last Modified: Sat, 17 May 2025 08:30:48 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.1` - unknown; unknown

```console
$ docker pull api-firewall@sha256:8d3190c047c20f37e36eba08ffb014d3e201500b9d930d177ebae9c7ce74a79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 KB (170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7509a9af91f6a18ca9360ab84a8124695499f61ecfc0f0e69821963361997d`

```dockerfile
```

-	Layers:
	-	`sha256:b3c7578d5971feebbe210f459acdfd5500f375e2c1f8b3f672d890b7fc411f60`  
		Last Modified: Wed, 23 Apr 2025 17:09:28 GMT  
		Size: 157.3 KB (157312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcae6e82dd4b020dd4dd1c936e3d7de5fefb2989c3c7213f2b1989f269e98c08`  
		Last Modified: Wed, 23 Apr 2025 17:09:28 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.1` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:415e3537a0b5bad79477d42c8c8d50a3f272d41d56ed459a0df8579aa0883cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15734454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032dc101fd578c0eff3254b5788bd4b3dd8c3aadbdd679fddeb3ee20a67c0b20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70884266db51b7be08ec72170fc9d2a77ba43353ceb1c6e247f1b5b97f3b8acf`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2648f0ca1e8826753dcdea0ef9ed907835fcfcd4d7edaed014d82ddff0109ce0`  
		Last Modified: Wed, 23 Apr 2025 17:08:42 GMT  
		Size: 11.7 MB (11740174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa080f8d12d2a0fedc6fa7cbd2a287c9e60608df30d920ba370304969c376c`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.1` - unknown; unknown

```console
$ docker pull api-firewall@sha256:b98b73cd69dea4cd271708849ebc00cdc831b1d268fd5af43a62da8f018f2f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 KB (170985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eb8eb1eb760989f14b46e41405fdce42243b1a016a7de01278dec253052a49`

```dockerfile
```

-	Layers:
	-	`sha256:e6cf2200a33eb13b57996d95285a819fe37080c10bab1c716707ba18d501d8fb`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 157.3 KB (157344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee75be37c17bc62332fb187868a6cf71153b40fbd403c7975794ec58f313dabe`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.1` - linux; 386

```console
$ docker pull api-firewall@sha256:30ef1e7c347b4fcc1ca14bd51dbf46fec940f41c1eb67fa407c1e40d3ea13f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14631357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdae8838df3c99be34fba525a7e676d73ac2cec058b117dabfd3b538ddae4095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921dcad93be766e0abb0bffa47d0b14ccbc29117e0e3d9aa1305dd2309339a25`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15e493b03a97fa2584a2ca8e164a699c89284009d8acbfdd4e3c05d6287bf5e`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 11.2 MB (11166485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49142d9c6951663dbabe38de9839425e599406d3bdf8ca8164ae349455701743`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.1` - unknown; unknown

```console
$ docker pull api-firewall@sha256:86d3924638cd4ddf0f23592091de08eac4542585cbefd3d4fcb57f1b429e5538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 KB (170819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c494d16f7e7d5c1374dc697493fce1aa661e2df98a086e71c76e86707a68fdb`

```dockerfile
```

-	Layers:
	-	`sha256:812a42e45c3e14c1bd57d0610b133beb326954acc31becd7606cab1e4ed0e35e`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 157.3 KB (157297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f72b5b22046d38ae9edb04fffa610e214e7db205fbfbc0bc23d7e5ed02e39f`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:be771f0ac41500b1db84c7aa5773f7e44bf7ac53aa0fe42ed63d759ec15e0d03
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
$ docker pull api-firewall@sha256:adc2e53fd6bf37ab18766bde17f72da1d83ee109b0ee1388629bfd4f0d0abb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16378778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7522389418bd410eaf0586d52cd05a374f8d2162315bd51059fa48c2da06a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd98c535a67674bd4022b684a1389cdd494562ae9ef6489321c54ff5c8b7b0`  
		Last Modified: Sat, 17 May 2025 08:30:47 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094363e0132e2f4d62d846596c6b692992e5eb918141b7336e2dea5b8ca0d49d`  
		Last Modified: Sat, 17 May 2025 08:30:47 GMT  
		Size: 12.7 MB (12735277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819981fe71ee9f7f73ddc8cb1ea55748e61c34ac63550cd35a211524f2ed3083`  
		Last Modified: Sat, 17 May 2025 08:30:48 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:8d3190c047c20f37e36eba08ffb014d3e201500b9d930d177ebae9c7ce74a79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 KB (170858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7509a9af91f6a18ca9360ab84a8124695499f61ecfc0f0e69821963361997d`

```dockerfile
```

-	Layers:
	-	`sha256:b3c7578d5971feebbe210f459acdfd5500f375e2c1f8b3f672d890b7fc411f60`  
		Last Modified: Wed, 23 Apr 2025 17:09:28 GMT  
		Size: 157.3 KB (157312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcae6e82dd4b020dd4dd1c936e3d7de5fefb2989c3c7213f2b1989f269e98c08`  
		Last Modified: Wed, 23 Apr 2025 17:09:28 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:415e3537a0b5bad79477d42c8c8d50a3f272d41d56ed459a0df8579aa0883cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15734454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032dc101fd578c0eff3254b5788bd4b3dd8c3aadbdd679fddeb3ee20a67c0b20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70884266db51b7be08ec72170fc9d2a77ba43353ceb1c6e247f1b5b97f3b8acf`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2648f0ca1e8826753dcdea0ef9ed907835fcfcd4d7edaed014d82ddff0109ce0`  
		Last Modified: Wed, 23 Apr 2025 17:08:42 GMT  
		Size: 11.7 MB (11740174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa080f8d12d2a0fedc6fa7cbd2a287c9e60608df30d920ba370304969c376c`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:b98b73cd69dea4cd271708849ebc00cdc831b1d268fd5af43a62da8f018f2f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 KB (170985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eb8eb1eb760989f14b46e41405fdce42243b1a016a7de01278dec253052a49`

```dockerfile
```

-	Layers:
	-	`sha256:e6cf2200a33eb13b57996d95285a819fe37080c10bab1c716707ba18d501d8fb`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 157.3 KB (157344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee75be37c17bc62332fb187868a6cf71153b40fbd403c7975794ec58f313dabe`  
		Last Modified: Wed, 23 Apr 2025 17:08:41 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:30ef1e7c347b4fcc1ca14bd51dbf46fec940f41c1eb67fa407c1e40d3ea13f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14631357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdae8838df3c99be34fba525a7e676d73ac2cec058b117dabfd3b538ddae4095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921dcad93be766e0abb0bffa47d0b14ccbc29117e0e3d9aa1305dd2309339a25`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15e493b03a97fa2584a2ca8e164a699c89284009d8acbfdd4e3c05d6287bf5e`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 11.2 MB (11166485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49142d9c6951663dbabe38de9839425e599406d3bdf8ca8164ae349455701743`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:86d3924638cd4ddf0f23592091de08eac4542585cbefd3d4fcb57f1b429e5538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 KB (170819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c494d16f7e7d5c1374dc697493fce1aa661e2df98a086e71c76e86707a68fdb`

```dockerfile
```

-	Layers:
	-	`sha256:812a42e45c3e14c1bd57d0610b133beb326954acc31becd7606cab1e4ed0e35e`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 157.3 KB (157297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f72b5b22046d38ae9edb04fffa610e214e7db205fbfbc0bc23d7e5ed02e39f`  
		Last Modified: Wed, 23 Apr 2025 17:09:26 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json
