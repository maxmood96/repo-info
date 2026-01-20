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
$ docker pull kapacitor@sha256:8b02d8e0ba02cde56d1a104ba227c578e0e52eec6d37b8206c8d4aaf3ed9ae1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:c88aecc684c4dd1da6d9fd8286d8d59f51baf5dd5ca079553333147e94469fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157663032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af03cbfd87de1e81c7b11fb06a7e902b70e00bff2efe10ac359994f9230b16a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:16:16 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:16 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f64ee49ae86a8609207d68c3ddf6230af2d9e770ca3b155cda2b45dd97629`  
		Last Modified: Thu, 15 Jan 2026 23:16:31 GMT  
		Size: 49.0 MB (48970801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16704bd5bb7d865c187ac1f527d937e86ffec3c50ee4cc3beaef6cf70f91e52f`  
		Last Modified: Thu, 15 Jan 2026 23:16:32 GMT  
		Size: 72.1 MB (72051145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af534873430c73d8e79450df6e2df84135fec105f9c1ef8c2f96d38d4ed5ee1`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf625e605f4adfd7fc6753244529c55dff81825ff50ae5e7aa5405103e1548d`  
		Last Modified: Thu, 15 Jan 2026 23:16:37 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:12e42e0a59763ced958976290230f0b2e6416505b48a563a27323ddc99dcf912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ffd2f2d16c7286307ce0545156b0d98a7e16108b5841231feca322f92c567`

```dockerfile
```

-	Layers:
	-	`sha256:53909e7d18b2311a090eb0c22ebd28650e2d7dda19c31d07a1e3daca12ba70c3`  
		Last Modified: Fri, 16 Jan 2026 02:22:18 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2754e29c97a8a8dee81e854e16b250e547f911edf2709269bf86fd3d25331839`  
		Last Modified: Fri, 16 Jan 2026 02:22:19 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e2070fa539333d6e2318c8e992fdd0364dc51bcaf6ad02b046d1612534fad6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149466694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17dfa9099d2055320ea8cc71dcf1fc4cf6b0087c7a6f847d0502a6ea4add60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:21:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:41 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce866c5b77da86a9383d2583a9a42c1b21e86f746ee7c6ac2c3308553a422b`  
		Last Modified: Thu, 15 Jan 2026 23:22:09 GMT  
		Size: 47.2 MB (47213869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd89a8870a2fd246249c5fa0017b4693e0a678bcedfec979a85760f2d20f8f5`  
		Last Modified: Thu, 15 Jan 2026 23:22:10 GMT  
		Size: 67.8 MB (67813752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec193a4f26362c7e7cfb88e3943f5b44b0668a7e2ee8fbe016b431f2874db8f5`  
		Last Modified: Thu, 15 Jan 2026 23:22:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301854c7bb29b4e6b1603b318fb0dc116fbb002c4d2870ff7fd9a1579a1b960`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:822d37928e086cb62f6ff29080642ff866595cd457e31ed59f886be551039994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ea2f90cdfec6b65ece9935a0c16d03faa0b5bc3ca39a27712a15d159c0f43`

```dockerfile
```

-	Layers:
	-	`sha256:32ed23bfe28b986ebda85169020cef5fbc227f7c73cbc9c2c62428a9cb0ffa5d`  
		Last Modified: Fri, 16 Jan 2026 02:22:23 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a48b7287700452437811e491f43e4d7f2f8dc3e36d84051cafcef4604e3ffcd`  
		Last Modified: Thu, 15 Jan 2026 23:21:54 GMT  
		Size: 14.8 KB (14809 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Tue, 09 Dec 2025 12:08:56 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
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
		Last Modified: Mon, 15 Dec 2025 09:52:30 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Mon, 15 Dec 2025 09:52:30 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:8b02d8e0ba02cde56d1a104ba227c578e0e52eec6d37b8206c8d4aaf3ed9ae1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:c88aecc684c4dd1da6d9fd8286d8d59f51baf5dd5ca079553333147e94469fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157663032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af03cbfd87de1e81c7b11fb06a7e902b70e00bff2efe10ac359994f9230b16a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:16:16 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:16 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f64ee49ae86a8609207d68c3ddf6230af2d9e770ca3b155cda2b45dd97629`  
		Last Modified: Thu, 15 Jan 2026 23:16:31 GMT  
		Size: 49.0 MB (48970801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16704bd5bb7d865c187ac1f527d937e86ffec3c50ee4cc3beaef6cf70f91e52f`  
		Last Modified: Thu, 15 Jan 2026 23:16:32 GMT  
		Size: 72.1 MB (72051145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af534873430c73d8e79450df6e2df84135fec105f9c1ef8c2f96d38d4ed5ee1`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf625e605f4adfd7fc6753244529c55dff81825ff50ae5e7aa5405103e1548d`  
		Last Modified: Thu, 15 Jan 2026 23:16:37 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:12e42e0a59763ced958976290230f0b2e6416505b48a563a27323ddc99dcf912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ffd2f2d16c7286307ce0545156b0d98a7e16108b5841231feca322f92c567`

```dockerfile
```

-	Layers:
	-	`sha256:53909e7d18b2311a090eb0c22ebd28650e2d7dda19c31d07a1e3daca12ba70c3`  
		Last Modified: Fri, 16 Jan 2026 02:22:18 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2754e29c97a8a8dee81e854e16b250e547f911edf2709269bf86fd3d25331839`  
		Last Modified: Fri, 16 Jan 2026 02:22:19 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e2070fa539333d6e2318c8e992fdd0364dc51bcaf6ad02b046d1612534fad6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149466694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17dfa9099d2055320ea8cc71dcf1fc4cf6b0087c7a6f847d0502a6ea4add60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:21:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:41 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce866c5b77da86a9383d2583a9a42c1b21e86f746ee7c6ac2c3308553a422b`  
		Last Modified: Thu, 15 Jan 2026 23:22:09 GMT  
		Size: 47.2 MB (47213869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd89a8870a2fd246249c5fa0017b4693e0a678bcedfec979a85760f2d20f8f5`  
		Last Modified: Thu, 15 Jan 2026 23:22:10 GMT  
		Size: 67.8 MB (67813752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec193a4f26362c7e7cfb88e3943f5b44b0668a7e2ee8fbe016b431f2874db8f5`  
		Last Modified: Thu, 15 Jan 2026 23:22:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301854c7bb29b4e6b1603b318fb0dc116fbb002c4d2870ff7fd9a1579a1b960`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:822d37928e086cb62f6ff29080642ff866595cd457e31ed59f886be551039994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ea2f90cdfec6b65ece9935a0c16d03faa0b5bc3ca39a27712a15d159c0f43`

```dockerfile
```

-	Layers:
	-	`sha256:32ed23bfe28b986ebda85169020cef5fbc227f7c73cbc9c2c62428a9cb0ffa5d`  
		Last Modified: Fri, 16 Jan 2026 02:22:23 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a48b7287700452437811e491f43e4d7f2f8dc3e36d84051cafcef4604e3ffcd`  
		Last Modified: Thu, 15 Jan 2026 23:21:54 GMT  
		Size: 14.8 KB (14809 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Tue, 09 Dec 2025 12:08:56 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
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
		Last Modified: Mon, 15 Dec 2025 09:52:30 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Mon, 15 Dec 2025 09:52:30 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:54 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:17:00 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Fri, 16 Jan 2026 02:22:31 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Fri, 16 Jan 2026 02:22:32 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:26 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:21 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Fri, 16 Jan 2026 02:22:37 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Fri, 16 Jan 2026 02:22:38 GMT  
		Size: 15.1 KB (15127 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7e96b276e6fd298eced341ccd6913904d9d82f6111d0a200988852d2b8c18f`  
		Last Modified: Tue, 09 Dec 2025 03:43:45 GMT  
		Size: 314.6 KB (314625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85135899b03878a7658cbe00b1009fbe5eea34be7549da7a0bfdbc6e99627fa`  
		Last Modified: Wed, 08 Oct 2025 23:10:54 GMT  
		Size: 88.1 MB (88132632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0111c1fb434318a62dca36307c313dce6ad95243af2299e946dddb7d786b4c`  
		Last Modified: Tue, 09 Dec 2025 03:43:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64252be71463e34a14ca8deca0ea44cabfb839ba164deba5f00925c82d7a51`  
		Last Modified: Tue, 09 Dec 2025 03:43:45 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:52 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4936a85adceea45586d7dcf8fcdcc3c775c585be14ed8ab94f40db7bb1b99ca3`  
		Last Modified: Mon, 08 Dec 2025 03:44:42 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.2` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:54 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:17:00 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Fri, 16 Jan 2026 02:22:31 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Fri, 16 Jan 2026 02:22:32 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.2` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:26 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:21 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Fri, 16 Jan 2026 02:22:37 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Fri, 16 Jan 2026 02:22:38 GMT  
		Size: 15.1 KB (15127 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7e96b276e6fd298eced341ccd6913904d9d82f6111d0a200988852d2b8c18f`  
		Last Modified: Tue, 09 Dec 2025 03:43:45 GMT  
		Size: 314.6 KB (314625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85135899b03878a7658cbe00b1009fbe5eea34be7549da7a0bfdbc6e99627fa`  
		Last Modified: Wed, 08 Oct 2025 23:10:54 GMT  
		Size: 88.1 MB (88132632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0111c1fb434318a62dca36307c313dce6ad95243af2299e946dddb7d786b4c`  
		Last Modified: Tue, 09 Dec 2025 03:43:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64252be71463e34a14ca8deca0ea44cabfb839ba164deba5f00925c82d7a51`  
		Last Modified: Tue, 09 Dec 2025 03:43:45 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:52 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4936a85adceea45586d7dcf8fcdcc3c775c585be14ed8ab94f40db7bb1b99ca3`  
		Last Modified: Mon, 08 Dec 2025 03:44:42 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Tue, 09 Dec 2025 12:08:56 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
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
		Last Modified: Mon, 15 Dec 2025 09:52:30 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Mon, 15 Dec 2025 09:52:30 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:54 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:17:00 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Fri, 16 Jan 2026 02:22:31 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Fri, 16 Jan 2026 02:22:32 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:26 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:21 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Fri, 16 Jan 2026 02:22:37 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Fri, 16 Jan 2026 02:22:38 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
