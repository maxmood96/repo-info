<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.8.9`](#api-firewall089)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.8.9`

```console
$ docker pull api-firewall@sha256:e41ab5d146514468d006d8f85a4ed64601b28f014afa3b68a756e2aa8de5568b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.8.9` - linux; amd64

```console
$ docker pull api-firewall@sha256:1b692154d00e9391e1afe0567ffa973dea816eac1007eae940044eeb799b3a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15942033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189e2a7af5fc53c36751c94bb027deb2022e3ffd1d6a7d0bc20aff33d4845440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFIREWALL_VERSION=v0.8.9
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='96e11e639f595fd72c9b4751a9ac49c8f0cbad40aa2987b14ea153c7dec3e935';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='d03cff5c58b6506f26643e41fadb9891b1d2ce20928ce820da943202402628c0';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e32b4870049d07957cea181c4842bba2b41a387f137ba0170b6a1bfc6137b33f';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
USER api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80334820dd21e72df4f80e1032acac7e642669967b64403a90d99386ab5231`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc18c269b3ee574ff838190745da7fae5edf0d984e456b632cc525e0ec66832`  
		Last Modified: Fri, 28 Mar 2025 22:01:53 GMT  
		Size: 12.3 MB (12298537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd54f2497c7c6dcb814af0c6d5621d8b6556d838f9715355f7e40e567ef2505`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.8.9` - unknown; unknown

```console
$ docker pull api-firewall@sha256:47e246d0924fae368651a6e010490699c183da28d1fe79d1772449987de33607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 KB (160466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b3e2195759e4e81b93dba8dc337d1e9c4cef0b13034e1bfd42ed04684ebabd`

```dockerfile
```

-	Layers:
	-	`sha256:8eab9f9cd2cff7cc59b045876e9e97bf82e3a233405fa8a5af0d77224709f863`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 146.9 KB (146920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8773b1b834d8dc6d132bba204519aefc3430639d9e5a3be647b40ba5b185813a`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.8.9` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:34d7e5b288071e62092e4bb03dae8660911556a636a6d7ab6b5c1ea5516e700d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15344264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571f43246808a6c3fd7d00423daa226bbc509647383dbdbb8e44e4fe21daf47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFIREWALL_VERSION=v0.8.9
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='96e11e639f595fd72c9b4751a9ac49c8f0cbad40aa2987b14ea153c7dec3e935';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='d03cff5c58b6506f26643e41fadb9891b1d2ce20928ce820da943202402628c0';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e32b4870049d07957cea181c4842bba2b41a387f137ba0170b6a1bfc6137b33f';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
USER api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
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
	-	`sha256:60885a05f224cf9fc656d4ac2d9f328d60c4c9c15ed902519000b162e5115e57`  
		Last Modified: Fri, 28 Mar 2025 22:01:38 GMT  
		Size: 11.3 MB (11349985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912ea81673319930f41cc16f4d83d2f940ce40884bf81345908d7768d219540`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.8.9` - unknown; unknown

```console
$ docker pull api-firewall@sha256:4044961208557b4dee2a96ac0d06bccb9c37470c484cda0cf231c2f5b717b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 KB (160593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023fb099eee2099fa8c08ead2912f7864e6d69561287c3af127f639d3c8b9f94`

```dockerfile
```

-	Layers:
	-	`sha256:c1fd9dea85113208546f620ce834c45c1bb1989a8e4dd5abd98e4b9d451e0f39`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 147.0 KB (146952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb2fa510f38082d49f0dd8e30c2452aaefbf0de756134b54ca5285b06e0e5f0`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.8.9` - linux; 386

```console
$ docker pull api-firewall@sha256:a3b6d55cc2f5c3a89733adca465518cf06157f408e728dad0aed9fee858f0958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14231118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bb47d63bf2c0b86bd295bdb319389fe5557b7a7cbd40a04376417fe0dcb71b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFIREWALL_VERSION=v0.8.9
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='96e11e639f595fd72c9b4751a9ac49c8f0cbad40aa2987b14ea153c7dec3e935';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='d03cff5c58b6506f26643e41fadb9891b1d2ce20928ce820da943202402628c0';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e32b4870049d07957cea181c4842bba2b41a387f137ba0170b6a1bfc6137b33f';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
USER api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b989bfecbde75cff4018a701f3d3cbd5fc60cbd9da88c06410f3abd2f47a0`  
		Last Modified: Fri, 28 Mar 2025 22:01:54 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487aa4ce3af2c15eddc83f02d9eb0657bf162dcf2e87f84370719025efe34175`  
		Last Modified: Fri, 28 Mar 2025 22:01:55 GMT  
		Size: 10.8 MB (10766243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4cf0e1ab85d755df7b11f70e7ceec267022acfe49f89d195e24a7dfbb0c998`  
		Last Modified: Fri, 28 Mar 2025 22:01:54 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.8.9` - unknown; unknown

```console
$ docker pull api-firewall@sha256:3c2da0608f889e9c5e636218a9b61878cb084910e37ee00370432064164d0e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 KB (160426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50d8014b53abdfa6a62e792ee3143a0e5f55998bc03998c2d6d68db6958ad9d`

```dockerfile
```

-	Layers:
	-	`sha256:45c693e990560e1d53cd0b5556a69eb858894cd621994fa609f8d20e571757ca`  
		Last Modified: Fri, 28 Mar 2025 22:01:55 GMT  
		Size: 146.9 KB (146905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fa00a525fcd28bdb5033b97b462148036b2a02d6e91cf143ae178bc84f2d4f`  
		Last Modified: Fri, 28 Mar 2025 22:01:54 GMT  
		Size: 13.5 KB (13521 bytes)  
		MIME: application/vnd.in-toto+json

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:e41ab5d146514468d006d8f85a4ed64601b28f014afa3b68a756e2aa8de5568b
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
$ docker pull api-firewall@sha256:1b692154d00e9391e1afe0567ffa973dea816eac1007eae940044eeb799b3a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15942033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189e2a7af5fc53c36751c94bb027deb2022e3ffd1d6a7d0bc20aff33d4845440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFIREWALL_VERSION=v0.8.9
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='96e11e639f595fd72c9b4751a9ac49c8f0cbad40aa2987b14ea153c7dec3e935';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='d03cff5c58b6506f26643e41fadb9891b1d2ce20928ce820da943202402628c0';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e32b4870049d07957cea181c4842bba2b41a387f137ba0170b6a1bfc6137b33f';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
USER api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80334820dd21e72df4f80e1032acac7e642669967b64403a90d99386ab5231`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc18c269b3ee574ff838190745da7fae5edf0d984e456b632cc525e0ec66832`  
		Last Modified: Fri, 28 Mar 2025 22:01:53 GMT  
		Size: 12.3 MB (12298537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd54f2497c7c6dcb814af0c6d5621d8b6556d838f9715355f7e40e567ef2505`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:47e246d0924fae368651a6e010490699c183da28d1fe79d1772449987de33607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 KB (160466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b3e2195759e4e81b93dba8dc337d1e9c4cef0b13034e1bfd42ed04684ebabd`

```dockerfile
```

-	Layers:
	-	`sha256:8eab9f9cd2cff7cc59b045876e9e97bf82e3a233405fa8a5af0d77224709f863`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 146.9 KB (146920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8773b1b834d8dc6d132bba204519aefc3430639d9e5a3be647b40ba5b185813a`  
		Last Modified: Fri, 28 Mar 2025 22:01:51 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:34d7e5b288071e62092e4bb03dae8660911556a636a6d7ab6b5c1ea5516e700d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15344264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571f43246808a6c3fd7d00423daa226bbc509647383dbdbb8e44e4fe21daf47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFIREWALL_VERSION=v0.8.9
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='96e11e639f595fd72c9b4751a9ac49c8f0cbad40aa2987b14ea153c7dec3e935';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='d03cff5c58b6506f26643e41fadb9891b1d2ce20928ce820da943202402628c0';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e32b4870049d07957cea181c4842bba2b41a387f137ba0170b6a1bfc6137b33f';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
USER api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
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
	-	`sha256:60885a05f224cf9fc656d4ac2d9f328d60c4c9c15ed902519000b162e5115e57`  
		Last Modified: Fri, 28 Mar 2025 22:01:38 GMT  
		Size: 11.3 MB (11349985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912ea81673319930f41cc16f4d83d2f940ce40884bf81345908d7768d219540`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:4044961208557b4dee2a96ac0d06bccb9c37470c484cda0cf231c2f5b717b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 KB (160593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023fb099eee2099fa8c08ead2912f7864e6d69561287c3af127f639d3c8b9f94`

```dockerfile
```

-	Layers:
	-	`sha256:c1fd9dea85113208546f620ce834c45c1bb1989a8e4dd5abd98e4b9d451e0f39`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 147.0 KB (146952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb2fa510f38082d49f0dd8e30c2452aaefbf0de756134b54ca5285b06e0e5f0`  
		Last Modified: Fri, 28 Mar 2025 22:01:37 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:a3b6d55cc2f5c3a89733adca465518cf06157f408e728dad0aed9fee858f0958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14231118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bb47d63bf2c0b86bd295bdb319389fe5557b7a7cbd40a04376417fe0dcb71b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
ENV APIFIREWALL_VERSION=v0.8.9
# Fri, 28 Mar 2025 19:03:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='96e11e639f595fd72c9b4751a9ac49c8f0cbad40aa2987b14ea153c7dec3e935';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='d03cff5c58b6506f26643e41fadb9891b1d2ce20928ce820da943202402628c0';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e32b4870049d07957cea181c4842bba2b41a387f137ba0170b6a1bfc6137b33f';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Fri, 28 Mar 2025 19:03:54 GMT
USER api-firewall
# Fri, 28 Mar 2025 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 19:03:54 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b989bfecbde75cff4018a701f3d3cbd5fc60cbd9da88c06410f3abd2f47a0`  
		Last Modified: Fri, 28 Mar 2025 22:01:54 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487aa4ce3af2c15eddc83f02d9eb0657bf162dcf2e87f84370719025efe34175`  
		Last Modified: Fri, 28 Mar 2025 22:01:55 GMT  
		Size: 10.8 MB (10766243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4cf0e1ab85d755df7b11f70e7ceec267022acfe49f89d195e24a7dfbb0c998`  
		Last Modified: Fri, 28 Mar 2025 22:01:54 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:3c2da0608f889e9c5e636218a9b61878cb084910e37ee00370432064164d0e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 KB (160426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50d8014b53abdfa6a62e792ee3143a0e5f55998bc03998c2d6d68db6958ad9d`

```dockerfile
```

-	Layers:
	-	`sha256:45c693e990560e1d53cd0b5556a69eb858894cd621994fa609f8d20e571757ca`  
		Last Modified: Fri, 28 Mar 2025 22:01:55 GMT  
		Size: 146.9 KB (146905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fa00a525fcd28bdb5033b97b462148036b2a02d6e91cf143ae178bc84f2d4f`  
		Last Modified: Fri, 28 Mar 2025 22:01:54 GMT  
		Size: 13.5 KB (13521 bytes)  
		MIME: application/vnd.in-toto+json
