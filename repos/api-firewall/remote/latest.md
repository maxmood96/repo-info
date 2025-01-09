## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:102b6abea6996982225644dee53825fb09ecbe206af73c132ce75fcc458d50ab
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
$ docker pull api-firewall@sha256:c4530ca0d49f7cd23e682dd0cdb239ce2c7fd132b4b329085725fa918c58cfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14871330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dae6f6283f77d666b1137c50f606875bc1909c31849bb12e077b42658abce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6dbfa79fb53abbdf09066e460642a2eefe0fd22d4d689f445d0b8d6a359c12`  
		Last Modified: Wed, 08 Jan 2025 17:57:31 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9d3842d666c42e2e44d6a2d60a3c8d753bed31d551eaf0e6e111fc5372fe7`  
		Last Modified: Wed, 08 Jan 2025 17:57:32 GMT  
		Size: 11.2 MB (11228353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fd9412dd32bdcb786c457c86c1c084dbfac4f4e273a726322bf9b5fc38ded`  
		Last Modified: Wed, 08 Jan 2025 17:57:31 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:90f8a58c604223d448b72b47f1d51a2b353de9b43cb20abf2c8dea65aae80521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (157955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129697e360438fbc8ad39185eed266212bd70492d995691498f7920a449ccbb0`

```dockerfile
```

-	Layers:
	-	`sha256:cf35ded3bc3a962a84df6900392f8c6748f205a2026e68606e36a1631dd118d5`  
		Last Modified: Wed, 08 Jan 2025 17:57:31 GMT  
		Size: 144.4 KB (144409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6967d06c0135baa9b8f8e444bec47f1b64d52117f6749d9c2072577c98d5e9`  
		Last Modified: Wed, 08 Jan 2025 17:57:31 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:57140ec8a6d965c22b481bfe5be35569aadb3e9619f1addf25aed46da55c33bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14351960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1aa65d60600f5edf3e992e30d3cdd128f11aa9d0908717af1cd478f8173997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d0395aaa7f38fd2896630a4de671efd70d9fbd96d428254351a941ea5bd731`  
		Last Modified: Wed, 08 Jan 2025 18:05:54 GMT  
		Size: 906.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452720089bb123a26c1620029c62c562c856e8f2953e26ecc86c75ce382d906`  
		Last Modified: Wed, 08 Jan 2025 18:05:55 GMT  
		Size: 10.4 MB (10358345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ca9a8080b3684bb16125d773554a1b50d7bf2394a19c5720d5b56b969acf8d`  
		Last Modified: Wed, 08 Jan 2025 18:05:54 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:1a30ec56949df897774f614d6b7e4211068e89f09fb2d360ed1dd6c977cc81ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba62ff90ef749960319995411c804be5187e82164fc29eb9e4ecfba932d0d08d`

```dockerfile
```

-	Layers:
	-	`sha256:c276ecf7f17ee35bb8814d75c6f329b02d32c6fa67107c2c6c7ec4478a3a71c8`  
		Last Modified: Wed, 08 Jan 2025 18:05:54 GMT  
		Size: 144.4 KB (144441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9a8b6b7a855d7016d49d6d987719d229d63533df39121395868742e6c277fe`  
		Last Modified: Wed, 08 Jan 2025 18:05:54 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:4a9662d3cf5221c5d166cbadf906e454215e3d86140faafdef7ddbdb62cf6d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13196366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5da4fb9f200e0bf46b9d43167470f25a13c358a53f74355e5565c8b7824feb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 20 Dec 2024 14:14:14 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c986ee084eed3a5427574ded9efe447b138a6f153c6d443350a7025d0e794c`  
		Last Modified: Wed, 08 Jan 2025 17:57:38 GMT  
		Size: 906.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b42615f1955b53832b907318c833b148ebc457dd0357990d63ab9fe21fa86b`  
		Last Modified: Wed, 08 Jan 2025 17:57:39 GMT  
		Size: 9.7 MB (9731979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50ea7f76c61ea8cdd2cb7f602998cf5a598b89340e005dd2e47d481382cb6d`  
		Last Modified: Wed, 08 Jan 2025 17:57:39 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:8bfcab98734c83e763e068d0801a12f6bacee079fdd8513a9be8e541ad6cbdf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 KB (157914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f16ef86f8b969d313c44e6a13b81497f38d51edd1522156e1098984fe1c353`

```dockerfile
```

-	Layers:
	-	`sha256:52dc561828c14e540fbad306aa06cab2edb79b8a7acd838af3cbfa232d58d613`  
		Last Modified: Wed, 08 Jan 2025 17:57:39 GMT  
		Size: 144.4 KB (144394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01118301e41aeb8ae4a4dab7c2ead962eed251638ac027d9747d9af7270c13f`  
		Last Modified: Wed, 08 Jan 2025 17:57:38 GMT  
		Size: 13.5 KB (13520 bytes)  
		MIME: application/vnd.in-toto+json
