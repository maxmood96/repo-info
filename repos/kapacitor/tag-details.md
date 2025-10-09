<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.2`](#kapacitor182)
-	[`kapacitor:1.8.2-alpine`](#kapacitor182-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:ae8b710dabcc1f01b2cf73481720f7bdf16d9c96b8457037b86b1f690e20f931
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:4f5ad29c2a5c0f20cee077e7c37158c548907a1fd2c8bade61054e87e4ff4823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156079256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed909ba814d8879695b8c71bf4c1a513ad7259b7e429b4da7282ac328904431`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c91da39938a99610071cb8f2424735e716b9f41a1d66250b87a6faa98a685`  
		Last Modified: Thu, 02 Oct 2025 09:29:32 GMT  
		Size: 47.4 MB (47384789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa471b0514df0090e87691badc5c0831de2bc659e7c884e214a13887937407dc`  
		Last Modified: Thu, 02 Oct 2025 09:29:51 GMT  
		Size: 72.1 MB (72051081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea85523e8034834952b4070f3ff42608ac2e40ec902ca31dba7eb2144d757801`  
		Last Modified: Thu, 02 Oct 2025 09:29:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12d92d1fc16ebfeeb0bad04fad7419db898ef5ce60cbcc56795b9aa6a352be`  
		Last Modified: Thu, 02 Oct 2025 09:29:28 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e86ebb4f25f946f8ab256eca2b925bc2bb0faa628b6b5988f4f9aa986104c00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d019a5691d2f2995d9c6aa46b7225c8b406e8caf5e484355abc2fd87daf24e19`

```dockerfile
```

-	Layers:
	-	`sha256:ed879a9e6245214d58c8bf88a1703143a070cf2ad9a015b56ffcd67e02038b29`  
		Last Modified: Thu, 02 Oct 2025 10:21:22 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5a9314b70eb585a7f9fa495a32f22317cec700d980b9fdd83cbdcc1712f5a0`  
		Last Modified: Thu, 02 Oct 2025 10:21:23 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e6311e3757d3afa10b467c7a464d79bca00d26908b107f39676c82a7707428c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147500678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb27e8ae6e6a0e6552fe8321c632c90506a2963b616a9cd948db504ecc0f2fd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9608fd74ba86b068e1f74b693e04cc006521cb5cd4f3d8205ba5da35454c0`  
		Last Modified: Thu, 02 Oct 2025 03:31:19 GMT  
		Size: 45.3 MB (45251170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da8397baad14f0a03eede13c0395aa0d6900ef583a3be42250bbac3888bedc6`  
		Last Modified: Thu, 02 Oct 2025 03:31:21 GMT  
		Size: 67.8 MB (67813765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4df7863a1c483743b6888c7ad0aa0903013afbdf98af262bf44dbacf8eff131`  
		Last Modified: Thu, 02 Oct 2025 03:16:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae1d5f12a889cd7412cb7953443f12287416320683fc138339c4581b83edb0a`  
		Last Modified: Thu, 02 Oct 2025 03:16:08 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cf89fa74acba440e2dac90efcddeabea227cbe55f473d8790037302ed93d69b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3cc363aa0e3b1dde07fc2bcf599fa8bd979dfc51bf65c0a2a38595b4f16220`

```dockerfile
```

-	Layers:
	-	`sha256:82a85ad3b9924708199f238a75fab69c7f0c00e6bf681cf59eef85ff2e4c5681`  
		Last Modified: Thu, 02 Oct 2025 04:21:26 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6474fb7ec987be9886bcde619e9833aca9e998d356c694d515f06db612ab0873`  
		Last Modified: Thu, 02 Oct 2025 04:21:27 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:4b29de73901134d65fb63d43ceb169ed217a41cea0013c2ce9d356a793b43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:32487036156063d2a292f41df2d6909ddcf587015ead7eddd26c6ff0efb6e193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75902966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b094251f0c804502e1fc81969c13c5e632d61bb3ea0d9b4682aa8ce4250ea3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 29 Sep 2025 12:39:49 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Wed, 08 Oct 2025 23:11:12 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a2272f84d134db7769109c42ab599628141be6e636573dd663a13347c6fa0064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c1306f8e81687ea167b0b39d7477517cca5b6b496fe11caa0ddeab5cf4363b`

```dockerfile
```

-	Layers:
	-	`sha256:3ef933bcc7ba9922e2fad7b96f23e7cc5beb964a2d4310c132b45e98d2dc09da`  
		Last Modified: Thu, 09 Oct 2025 01:21:16 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Thu, 09 Oct 2025 01:21:17 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:ae8b710dabcc1f01b2cf73481720f7bdf16d9c96b8457037b86b1f690e20f931
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:4f5ad29c2a5c0f20cee077e7c37158c548907a1fd2c8bade61054e87e4ff4823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156079256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed909ba814d8879695b8c71bf4c1a513ad7259b7e429b4da7282ac328904431`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c91da39938a99610071cb8f2424735e716b9f41a1d66250b87a6faa98a685`  
		Last Modified: Thu, 02 Oct 2025 09:29:32 GMT  
		Size: 47.4 MB (47384789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa471b0514df0090e87691badc5c0831de2bc659e7c884e214a13887937407dc`  
		Last Modified: Thu, 02 Oct 2025 09:29:51 GMT  
		Size: 72.1 MB (72051081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea85523e8034834952b4070f3ff42608ac2e40ec902ca31dba7eb2144d757801`  
		Last Modified: Thu, 02 Oct 2025 09:29:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12d92d1fc16ebfeeb0bad04fad7419db898ef5ce60cbcc56795b9aa6a352be`  
		Last Modified: Thu, 02 Oct 2025 09:29:28 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e86ebb4f25f946f8ab256eca2b925bc2bb0faa628b6b5988f4f9aa986104c00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d019a5691d2f2995d9c6aa46b7225c8b406e8caf5e484355abc2fd87daf24e19`

```dockerfile
```

-	Layers:
	-	`sha256:ed879a9e6245214d58c8bf88a1703143a070cf2ad9a015b56ffcd67e02038b29`  
		Last Modified: Thu, 02 Oct 2025 10:21:22 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5a9314b70eb585a7f9fa495a32f22317cec700d980b9fdd83cbdcc1712f5a0`  
		Last Modified: Thu, 02 Oct 2025 10:21:23 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e6311e3757d3afa10b467c7a464d79bca00d26908b107f39676c82a7707428c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147500678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb27e8ae6e6a0e6552fe8321c632c90506a2963b616a9cd948db504ecc0f2fd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9608fd74ba86b068e1f74b693e04cc006521cb5cd4f3d8205ba5da35454c0`  
		Last Modified: Thu, 02 Oct 2025 03:31:19 GMT  
		Size: 45.3 MB (45251170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da8397baad14f0a03eede13c0395aa0d6900ef583a3be42250bbac3888bedc6`  
		Last Modified: Thu, 02 Oct 2025 03:31:21 GMT  
		Size: 67.8 MB (67813765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4df7863a1c483743b6888c7ad0aa0903013afbdf98af262bf44dbacf8eff131`  
		Last Modified: Thu, 02 Oct 2025 03:16:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae1d5f12a889cd7412cb7953443f12287416320683fc138339c4581b83edb0a`  
		Last Modified: Thu, 02 Oct 2025 03:16:08 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cf89fa74acba440e2dac90efcddeabea227cbe55f473d8790037302ed93d69b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3cc363aa0e3b1dde07fc2bcf599fa8bd979dfc51bf65c0a2a38595b4f16220`

```dockerfile
```

-	Layers:
	-	`sha256:82a85ad3b9924708199f238a75fab69c7f0c00e6bf681cf59eef85ff2e4c5681`  
		Last Modified: Thu, 02 Oct 2025 04:21:26 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6474fb7ec987be9886bcde619e9833aca9e998d356c694d515f06db612ab0873`  
		Last Modified: Thu, 02 Oct 2025 04:21:27 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:4b29de73901134d65fb63d43ceb169ed217a41cea0013c2ce9d356a793b43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:32487036156063d2a292f41df2d6909ddcf587015ead7eddd26c6ff0efb6e193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75902966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b094251f0c804502e1fc81969c13c5e632d61bb3ea0d9b4682aa8ce4250ea3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 29 Sep 2025 12:39:49 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Wed, 08 Oct 2025 23:11:12 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a2272f84d134db7769109c42ab599628141be6e636573dd663a13347c6fa0064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c1306f8e81687ea167b0b39d7477517cca5b6b496fe11caa0ddeab5cf4363b`

```dockerfile
```

-	Layers:
	-	`sha256:3ef933bcc7ba9922e2fad7b96f23e7cc5beb964a2d4310c132b45e98d2dc09da`  
		Last Modified: Thu, 09 Oct 2025 01:21:16 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Thu, 09 Oct 2025 01:21:17 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:8af2e0665c886fb74eab9699d0c5e181780b97ebc394602dad769d571b1178d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:23031a4049af462089444100e0ea41824b461a759c41ad682cc34ccba3a6ba1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172240899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e118bfd7c2c125b56a6af5962a32f8954f62dede9e3fe9598ffa9cac10566e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2baee51d10ab242bbabf733dec920d0015113b400d7ae8c67d5035a28b277f5`  
		Last Modified: Thu, 02 Oct 2025 08:36:30 GMT  
		Size: 47.4 MB (47384790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb921dab1f7bdb605cb42ce6500764c079f9df48305ebdc58ddb038ff636a1e`  
		Last Modified: Thu, 02 Oct 2025 08:36:21 GMT  
		Size: 88.2 MB (88212722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f567a9ff438c98e298b0aef4081302afa33ac81dbbad6f22eb6917d67b4b5`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a2bee9150f2d4212c5bed686fb4934ff97f1bb08718e6b156c8996a8b49aa`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c9c5ed172664c8182f210b13fb7df231ff84948bd182ee3728d60afab8cbe63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc886c044e488c6e69ed8d7c70568b3a2954c385d81344e98487c3763b4d133`

```dockerfile
```

-	Layers:
	-	`sha256:9858f883ecd968d94ec2e1a7a47703f013277998ca3b3b78d546cbe48f135a32`  
		Last Modified: Thu, 02 Oct 2025 10:21:32 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ebac661d8ddc3ed5044c6b45c051a6d858bcbe8d19b4f94aad47568bae5e0`  
		Last Modified: Thu, 02 Oct 2025 10:21:33 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:c7a8eeb82ef4f15524e3cb6ae98cdfa36b641458c26265fe996d2c7f270146b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161696478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee2f70ec439fcb8ecc2bf60125fcf970f471c8ce1ae545d72aa617b4787f45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c027524204ede247971df3e55507c2a550b813d416efdf95e683767d420e91`  
		Last Modified: Thu, 02 Oct 2025 03:31:13 GMT  
		Size: 45.3 MB (45251049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca37f0340e18c9b768ee7d048b54cc869eb443c8fded3816cd4296ed0506e18`  
		Last Modified: Thu, 02 Oct 2025 03:31:18 GMT  
		Size: 82.0 MB (82009684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ebbd0ee3cbb9593982f755e6c46b7c8d47e36f563d13b3af6f9f0055da32c`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078fc759988b13ed983c52766c2e67f8a4b8f6b22d7c3b5d27eeca06ca2fe489`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3ba8b490ff1aa8ff3ddd28c5b889d312cd8fa4f6dedfe70a96b184f1a1c3d505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0499ba96e61ba17ddff758b7a0a21838df714f2fb9ddbf389dbd520d6256`

```dockerfile
```

-	Layers:
	-	`sha256:bc219b226c4662e9c83639d60188fe11bd7452b223036cd88061258d7904251c`  
		Last Modified: Thu, 02 Oct 2025 04:21:34 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51b3667b4235134c87bb7cda0ae91c3a7f085ed9aced27459a7b9d071f34f4e`  
		Last Modified: Thu, 02 Oct 2025 04:21:35 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:8543a93bfb1166a1ffe1dfb887ef265d653e11fcd5f2939829fe923b959c69d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:9bd4641a250a9090d93a72694a79caff33fe45107ce155e7d97d4ee9ebc2b1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92250506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06374e007c985e9f40f63849e7b8e2849566355b78bb57c62e222d4fc5d21db2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 29 Sep 2025 12:39:49 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7e96b276e6fd298eced341ccd6913904d9d82f6111d0a200988852d2b8c18f`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 314.6 KB (314625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85135899b03878a7658cbe00b1009fbe5eea34be7549da7a0bfdbc6e99627fa`  
		Last Modified: Wed, 08 Oct 2025 23:11:13 GMT  
		Size: 88.1 MB (88132632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0111c1fb434318a62dca36307c313dce6ad95243af2299e946dddb7d786b4c`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64252be71463e34a14ca8deca0ea44cabfb839ba164deba5f00925c82d7a51`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3b06536907d424c4754cdad37af2baa0fea9df4a7c4fe33004f660c1bd3bb8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e962a3ab2de9e559604691775ce9443a7fd34058d2147b406e8d1715d963daa`

```dockerfile
```

-	Layers:
	-	`sha256:91423496536bc7ff79e2ff925f63864dd28db1b546c42f9d9f6ecc9a4dedd69e`  
		Last Modified: Thu, 09 Oct 2025 01:21:24 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4936a85adceea45586d7dcf8fcdcc3c775c585be14ed8ab94f40db7bb1b99ca3`  
		Last Modified: Thu, 09 Oct 2025 01:21:25 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2`

```console
$ docker pull kapacitor@sha256:8af2e0665c886fb74eab9699d0c5e181780b97ebc394602dad769d571b1178d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.2` - linux; amd64

```console
$ docker pull kapacitor@sha256:23031a4049af462089444100e0ea41824b461a759c41ad682cc34ccba3a6ba1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172240899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e118bfd7c2c125b56a6af5962a32f8954f62dede9e3fe9598ffa9cac10566e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2baee51d10ab242bbabf733dec920d0015113b400d7ae8c67d5035a28b277f5`  
		Last Modified: Thu, 02 Oct 2025 08:36:30 GMT  
		Size: 47.4 MB (47384790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb921dab1f7bdb605cb42ce6500764c079f9df48305ebdc58ddb038ff636a1e`  
		Last Modified: Thu, 02 Oct 2025 08:36:21 GMT  
		Size: 88.2 MB (88212722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f567a9ff438c98e298b0aef4081302afa33ac81dbbad6f22eb6917d67b4b5`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a2bee9150f2d4212c5bed686fb4934ff97f1bb08718e6b156c8996a8b49aa`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c9c5ed172664c8182f210b13fb7df231ff84948bd182ee3728d60afab8cbe63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc886c044e488c6e69ed8d7c70568b3a2954c385d81344e98487c3763b4d133`

```dockerfile
```

-	Layers:
	-	`sha256:9858f883ecd968d94ec2e1a7a47703f013277998ca3b3b78d546cbe48f135a32`  
		Last Modified: Thu, 02 Oct 2025 10:21:32 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ebac661d8ddc3ed5044c6b45c051a6d858bcbe8d19b4f94aad47568bae5e0`  
		Last Modified: Thu, 02 Oct 2025 10:21:33 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.2` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:c7a8eeb82ef4f15524e3cb6ae98cdfa36b641458c26265fe996d2c7f270146b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161696478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee2f70ec439fcb8ecc2bf60125fcf970f471c8ce1ae545d72aa617b4787f45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c027524204ede247971df3e55507c2a550b813d416efdf95e683767d420e91`  
		Last Modified: Thu, 02 Oct 2025 03:31:13 GMT  
		Size: 45.3 MB (45251049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca37f0340e18c9b768ee7d048b54cc869eb443c8fded3816cd4296ed0506e18`  
		Last Modified: Thu, 02 Oct 2025 03:31:18 GMT  
		Size: 82.0 MB (82009684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ebbd0ee3cbb9593982f755e6c46b7c8d47e36f563d13b3af6f9f0055da32c`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078fc759988b13ed983c52766c2e67f8a4b8f6b22d7c3b5d27eeca06ca2fe489`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3ba8b490ff1aa8ff3ddd28c5b889d312cd8fa4f6dedfe70a96b184f1a1c3d505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0499ba96e61ba17ddff758b7a0a21838df714f2fb9ddbf389dbd520d6256`

```dockerfile
```

-	Layers:
	-	`sha256:bc219b226c4662e9c83639d60188fe11bd7452b223036cd88061258d7904251c`  
		Last Modified: Thu, 02 Oct 2025 04:21:34 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51b3667b4235134c87bb7cda0ae91c3a7f085ed9aced27459a7b9d071f34f4e`  
		Last Modified: Thu, 02 Oct 2025 04:21:35 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2-alpine`

```console
$ docker pull kapacitor@sha256:8543a93bfb1166a1ffe1dfb887ef265d653e11fcd5f2939829fe923b959c69d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.2-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:9bd4641a250a9090d93a72694a79caff33fe45107ce155e7d97d4ee9ebc2b1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92250506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06374e007c985e9f40f63849e7b8e2849566355b78bb57c62e222d4fc5d21db2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 29 Sep 2025 12:39:49 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7e96b276e6fd298eced341ccd6913904d9d82f6111d0a200988852d2b8c18f`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 314.6 KB (314625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85135899b03878a7658cbe00b1009fbe5eea34be7549da7a0bfdbc6e99627fa`  
		Last Modified: Wed, 08 Oct 2025 23:11:13 GMT  
		Size: 88.1 MB (88132632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0111c1fb434318a62dca36307c313dce6ad95243af2299e946dddb7d786b4c`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64252be71463e34a14ca8deca0ea44cabfb839ba164deba5f00925c82d7a51`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3b06536907d424c4754cdad37af2baa0fea9df4a7c4fe33004f660c1bd3bb8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e962a3ab2de9e559604691775ce9443a7fd34058d2147b406e8d1715d963daa`

```dockerfile
```

-	Layers:
	-	`sha256:91423496536bc7ff79e2ff925f63864dd28db1b546c42f9d9f6ecc9a4dedd69e`  
		Last Modified: Thu, 09 Oct 2025 01:21:24 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4936a85adceea45586d7dcf8fcdcc3c775c585be14ed8ab94f40db7bb1b99ca3`  
		Last Modified: Thu, 09 Oct 2025 01:21:25 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:4b29de73901134d65fb63d43ceb169ed217a41cea0013c2ce9d356a793b43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:32487036156063d2a292f41df2d6909ddcf587015ead7eddd26c6ff0efb6e193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75902966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b094251f0c804502e1fc81969c13c5e632d61bb3ea0d9b4682aa8ce4250ea3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 29 Sep 2025 12:39:49 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Wed, 08 Oct 2025 23:11:12 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a2272f84d134db7769109c42ab599628141be6e636573dd663a13347c6fa0064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c1306f8e81687ea167b0b39d7477517cca5b6b496fe11caa0ddeab5cf4363b`

```dockerfile
```

-	Layers:
	-	`sha256:3ef933bcc7ba9922e2fad7b96f23e7cc5beb964a2d4310c132b45e98d2dc09da`  
		Last Modified: Thu, 09 Oct 2025 01:21:16 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Thu, 09 Oct 2025 01:21:17 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:8af2e0665c886fb74eab9699d0c5e181780b97ebc394602dad769d571b1178d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:23031a4049af462089444100e0ea41824b461a759c41ad682cc34ccba3a6ba1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172240899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e118bfd7c2c125b56a6af5962a32f8954f62dede9e3fe9598ffa9cac10566e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2baee51d10ab242bbabf733dec920d0015113b400d7ae8c67d5035a28b277f5`  
		Last Modified: Thu, 02 Oct 2025 08:36:30 GMT  
		Size: 47.4 MB (47384790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb921dab1f7bdb605cb42ce6500764c079f9df48305ebdc58ddb038ff636a1e`  
		Last Modified: Thu, 02 Oct 2025 08:36:21 GMT  
		Size: 88.2 MB (88212722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f567a9ff438c98e298b0aef4081302afa33ac81dbbad6f22eb6917d67b4b5`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a2bee9150f2d4212c5bed686fb4934ff97f1bb08718e6b156c8996a8b49aa`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c9c5ed172664c8182f210b13fb7df231ff84948bd182ee3728d60afab8cbe63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc886c044e488c6e69ed8d7c70568b3a2954c385d81344e98487c3763b4d133`

```dockerfile
```

-	Layers:
	-	`sha256:9858f883ecd968d94ec2e1a7a47703f013277998ca3b3b78d546cbe48f135a32`  
		Last Modified: Thu, 02 Oct 2025 10:21:32 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ebac661d8ddc3ed5044c6b45c051a6d858bcbe8d19b4f94aad47568bae5e0`  
		Last Modified: Thu, 02 Oct 2025 10:21:33 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:c7a8eeb82ef4f15524e3cb6ae98cdfa36b641458c26265fe996d2c7f270146b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161696478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee2f70ec439fcb8ecc2bf60125fcf970f471c8ce1ae545d72aa617b4787f45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c027524204ede247971df3e55507c2a550b813d416efdf95e683767d420e91`  
		Last Modified: Thu, 02 Oct 2025 03:31:13 GMT  
		Size: 45.3 MB (45251049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca37f0340e18c9b768ee7d048b54cc869eb443c8fded3816cd4296ed0506e18`  
		Last Modified: Thu, 02 Oct 2025 03:31:18 GMT  
		Size: 82.0 MB (82009684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ebbd0ee3cbb9593982f755e6c46b7c8d47e36f563d13b3af6f9f0055da32c`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078fc759988b13ed983c52766c2e67f8a4b8f6b22d7c3b5d27eeca06ca2fe489`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3ba8b490ff1aa8ff3ddd28c5b889d312cd8fa4f6dedfe70a96b184f1a1c3d505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0499ba96e61ba17ddff758b7a0a21838df714f2fb9ddbf389dbd520d6256`

```dockerfile
```

-	Layers:
	-	`sha256:bc219b226c4662e9c83639d60188fe11bd7452b223036cd88061258d7904251c`  
		Last Modified: Thu, 02 Oct 2025 04:21:34 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51b3667b4235134c87bb7cda0ae91c3a7f085ed9aced27459a7b9d071f34f4e`  
		Last Modified: Thu, 02 Oct 2025 04:21:35 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
