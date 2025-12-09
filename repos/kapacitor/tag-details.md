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
$ docker pull kapacitor@sha256:e80cab7b92ba12cb3f2c1e2d0a048a9ff3453f9fdb7995140993c04a937b7e3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:506696e00443f7ab877be35e11dcbea94d1e6c6b2d2fb49403105be54bca560a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156942833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e6136e0a3c90db324c61f4115ddf6bd4e55ff611d42503192f621459e273d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:27:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 14 Nov 2025 00:28:02 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:02 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9285bcdb3d127ddfecb2e5ce1f9ef4327b0de7ad7a22f0f9d34ab33205283d0c`  
		Last Modified: Fri, 14 Nov 2025 00:28:30 GMT  
		Size: 48.2 MB (48248185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4da74907e523c9d7c3442a312ec2109182f1067dc875fd845e6f8594882a4e0`  
		Last Modified: Fri, 14 Nov 2025 00:28:37 GMT  
		Size: 72.1 MB (72051108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51a7db2cb695e903407dc6fef5fc26518034652775de15e9fb52aea90293a50`  
		Last Modified: Fri, 14 Nov 2025 00:28:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a57001999b396f47a70ef832477702e2d5663f9d491b772dff964151208d1d2`  
		Last Modified: Fri, 14 Nov 2025 00:28:24 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:fe19d4aa972249eac6e5ba9c597fc741a84a3d98f04e9b3052de4cbc296f6fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fedf2b314f89894feaf165ca4ba4eedf436a8351d217734cbb31e12e2316098`

```dockerfile
```

-	Layers:
	-	`sha256:e09983569e38d4de311e6da8960d1f7ed83fbbf11107520a0efee44afba6b7a5`  
		Last Modified: Fri, 14 Nov 2025 02:21:44 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451ab3b7f14e273cd38d063ef15a275f7a4ae15e32c4c6ae5dc39f2be6395891`  
		Last Modified: Fri, 14 Nov 2025 02:21:45 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5ba0e245321364985067bd7799f5bc6e4ea8c0d62d02d9c6b47c015f4eb79e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148554186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a12378274696a1a1bc8305b60b47363bf9a7b9a75d8637a81838cd9fb63ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 14 Nov 2025 00:28:13 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:13 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f62e10f5788f865c710d35dc0da71112ec293750a926aff58b860d783d9bf56`  
		Last Modified: Fri, 14 Nov 2025 00:28:36 GMT  
		Size: 46.3 MB (46303533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b844a9b23b4cf0e4559a3a79841f5ec9e97038b72ab1cb7412526b1730d18f1`  
		Last Modified: Fri, 14 Nov 2025 00:28:37 GMT  
		Size: 67.8 MB (67813759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccc35a4d4e8a46b5df6fb49947cf467128803020bb1c412122be9e75b323ae2`  
		Last Modified: Fri, 14 Nov 2025 00:28:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7243a6015ef4394821aca3f30cea4ecb26b36caf038463affd39d4da526b62`  
		Last Modified: Fri, 14 Nov 2025 00:28:33 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:57ae18744a15a04a69242641b4f02755e41159602ae78a3099a90c3ff4d5f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145ebd7874e804b9c65269b721d33f7a2ae45cbabfa15a1e6ec215f117d8dd98`

```dockerfile
```

-	Layers:
	-	`sha256:d9117456052e8416195a7dc0b7ff08a00f86a0ccc177d05a5396e55bc1c0262c`  
		Last Modified: Fri, 14 Nov 2025 02:21:50 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8df792bd62416ba531f4642eebf44d84e79dd3796ba773f6dc9bc3524ef029`  
		Last Modified: Fri, 14 Nov 2025 02:21:51 GMT  
		Size: 14.8 KB (14811 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:e80cab7b92ba12cb3f2c1e2d0a048a9ff3453f9fdb7995140993c04a937b7e3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:506696e00443f7ab877be35e11dcbea94d1e6c6b2d2fb49403105be54bca560a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156942833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e6136e0a3c90db324c61f4115ddf6bd4e55ff611d42503192f621459e273d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:27:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 14 Nov 2025 00:28:02 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:02 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9285bcdb3d127ddfecb2e5ce1f9ef4327b0de7ad7a22f0f9d34ab33205283d0c`  
		Last Modified: Fri, 14 Nov 2025 00:28:30 GMT  
		Size: 48.2 MB (48248185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4da74907e523c9d7c3442a312ec2109182f1067dc875fd845e6f8594882a4e0`  
		Last Modified: Fri, 14 Nov 2025 00:28:37 GMT  
		Size: 72.1 MB (72051108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51a7db2cb695e903407dc6fef5fc26518034652775de15e9fb52aea90293a50`  
		Last Modified: Fri, 14 Nov 2025 00:28:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a57001999b396f47a70ef832477702e2d5663f9d491b772dff964151208d1d2`  
		Last Modified: Fri, 14 Nov 2025 00:28:24 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:fe19d4aa972249eac6e5ba9c597fc741a84a3d98f04e9b3052de4cbc296f6fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fedf2b314f89894feaf165ca4ba4eedf436a8351d217734cbb31e12e2316098`

```dockerfile
```

-	Layers:
	-	`sha256:e09983569e38d4de311e6da8960d1f7ed83fbbf11107520a0efee44afba6b7a5`  
		Last Modified: Fri, 14 Nov 2025 02:21:44 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451ab3b7f14e273cd38d063ef15a275f7a4ae15e32c4c6ae5dc39f2be6395891`  
		Last Modified: Fri, 14 Nov 2025 02:21:45 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5ba0e245321364985067bd7799f5bc6e4ea8c0d62d02d9c6b47c015f4eb79e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148554186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a12378274696a1a1bc8305b60b47363bf9a7b9a75d8637a81838cd9fb63ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 14 Nov 2025 00:28:13 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:13 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f62e10f5788f865c710d35dc0da71112ec293750a926aff58b860d783d9bf56`  
		Last Modified: Fri, 14 Nov 2025 00:28:36 GMT  
		Size: 46.3 MB (46303533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b844a9b23b4cf0e4559a3a79841f5ec9e97038b72ab1cb7412526b1730d18f1`  
		Last Modified: Fri, 14 Nov 2025 00:28:37 GMT  
		Size: 67.8 MB (67813759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccc35a4d4e8a46b5df6fb49947cf467128803020bb1c412122be9e75b323ae2`  
		Last Modified: Fri, 14 Nov 2025 00:28:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7243a6015ef4394821aca3f30cea4ecb26b36caf038463affd39d4da526b62`  
		Last Modified: Fri, 14 Nov 2025 00:28:33 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:57ae18744a15a04a69242641b4f02755e41159602ae78a3099a90c3ff4d5f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145ebd7874e804b9c65269b721d33f7a2ae45cbabfa15a1e6ec215f117d8dd98`

```dockerfile
```

-	Layers:
	-	`sha256:d9117456052e8416195a7dc0b7ff08a00f86a0ccc177d05a5396e55bc1c0262c`  
		Last Modified: Fri, 14 Nov 2025 02:21:50 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8df792bd62416ba531f4642eebf44d84e79dd3796ba773f6dc9bc3524ef029`  
		Last Modified: Fri, 14 Nov 2025 02:21:51 GMT  
		Size: 14.8 KB (14811 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:7fa702d2444080c86ba6b0733286a7324800b4c0faa3177349b4852d7f93602a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:ad424b6437336383d6709f715fcc4d07447a25631933fff8ebf822c8b822ccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173104505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fcb0d2a2b24d7a2375a04baa29202f7c1dd9161e1024061225fc72f3b24caa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:08 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:08 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7135dbac77e480e19f2fab49d6bf449a7b00e25043f30204f2c35cbaf2081e`  
		Last Modified: Fri, 14 Nov 2025 00:28:35 GMT  
		Size: 48.2 MB (48248227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4667606aa22066eb1ead38518f235c333ee2336fb3ca2ac1e9be16644ca7e4cd`  
		Last Modified: Fri, 14 Nov 2025 00:28:41 GMT  
		Size: 88.2 MB (88212738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82416f38ec3797f036f93179be2ce2564f4204507898f04753b75730f39d8da1`  
		Last Modified: Fri, 14 Nov 2025 00:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de306879312a1e10fffc2828bfc33198774cbaaf6d943b4ff63f9ffa63c7a639`  
		Last Modified: Fri, 14 Nov 2025 00:28:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a7da07e90eadc8945c1c0cf7649e29a39ab734e3a29ad19d3018ec47d2c599e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a54ded414376942e7256e72a433b9d8afcb21ae4aecc958a903df8836ba5003`

```dockerfile
```

-	Layers:
	-	`sha256:4cba04e58c70efe1eba618345ae547556183fc88c902756df7a4c8c3928c2438`  
		Last Modified: Fri, 14 Nov 2025 02:21:57 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07e8b3b981f40dab492441333de3d022e7c2be22df664e320c2b50065dbe332`  
		Last Modified: Fri, 14 Nov 2025 02:21:58 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d0d87f6e0e8ae3377d4dd02dde6bbbcfedbda40aacf90bdb018ff091f604e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162750022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d05fb9a6cec856b762b1711ec4b5346c0d92050196a6152c416247d87409f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc514c00b5880177c45acb158773e3e0427cbf47b9e3ec5fe3976be52704a5a7`  
		Last Modified: Fri, 14 Nov 2025 00:28:52 GMT  
		Size: 46.3 MB (46303484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9e4b28f4c70b491bc425ae0c0b8fc849fc3a59ff25d3efa2fb9cf1a9bc76e6`  
		Last Modified: Fri, 14 Nov 2025 00:28:54 GMT  
		Size: 82.0 MB (82009642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df04f27e6295adef6bb6401f0ec49a56d23f939eb1e2cec9249cc69807c93d9c`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba64dc4b68645941b6e163791183152612fa0ebc92fee387fd4660750cabaa`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:01cc88792432f43c356679ae274fef28b207b3c1240b69c9dc3fe010ad2ff4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e95c87a147a28fed5df5662afaf5075e693a74b2b61815a98c2a2f78d7286`

```dockerfile
```

-	Layers:
	-	`sha256:a39870c15d12b577e34cfbba53326926f1c47027f4ff66efd70517a8a6e9b525`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e700bf823a01ee7b340e763219eb84fc053accb5b66c1ea64c45a2553bb236`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
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
		Last Modified: Tue, 09 Dec 2025 03:43:48 GMT  
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
		Last Modified: Mon, 08 Dec 2025 03:44:37 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4936a85adceea45586d7dcf8fcdcc3c775c585be14ed8ab94f40db7bb1b99ca3`  
		Last Modified: Mon, 08 Dec 2025 03:44:42 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2`

```console
$ docker pull kapacitor@sha256:7fa702d2444080c86ba6b0733286a7324800b4c0faa3177349b4852d7f93602a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.2` - linux; amd64

```console
$ docker pull kapacitor@sha256:ad424b6437336383d6709f715fcc4d07447a25631933fff8ebf822c8b822ccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173104505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fcb0d2a2b24d7a2375a04baa29202f7c1dd9161e1024061225fc72f3b24caa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:08 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:08 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7135dbac77e480e19f2fab49d6bf449a7b00e25043f30204f2c35cbaf2081e`  
		Last Modified: Fri, 14 Nov 2025 00:28:35 GMT  
		Size: 48.2 MB (48248227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4667606aa22066eb1ead38518f235c333ee2336fb3ca2ac1e9be16644ca7e4cd`  
		Last Modified: Fri, 14 Nov 2025 00:28:41 GMT  
		Size: 88.2 MB (88212738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82416f38ec3797f036f93179be2ce2564f4204507898f04753b75730f39d8da1`  
		Last Modified: Fri, 14 Nov 2025 00:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de306879312a1e10fffc2828bfc33198774cbaaf6d943b4ff63f9ffa63c7a639`  
		Last Modified: Fri, 14 Nov 2025 00:28:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a7da07e90eadc8945c1c0cf7649e29a39ab734e3a29ad19d3018ec47d2c599e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a54ded414376942e7256e72a433b9d8afcb21ae4aecc958a903df8836ba5003`

```dockerfile
```

-	Layers:
	-	`sha256:4cba04e58c70efe1eba618345ae547556183fc88c902756df7a4c8c3928c2438`  
		Last Modified: Fri, 14 Nov 2025 02:21:57 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07e8b3b981f40dab492441333de3d022e7c2be22df664e320c2b50065dbe332`  
		Last Modified: Fri, 14 Nov 2025 02:21:58 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.2` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d0d87f6e0e8ae3377d4dd02dde6bbbcfedbda40aacf90bdb018ff091f604e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162750022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d05fb9a6cec856b762b1711ec4b5346c0d92050196a6152c416247d87409f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc514c00b5880177c45acb158773e3e0427cbf47b9e3ec5fe3976be52704a5a7`  
		Last Modified: Fri, 14 Nov 2025 00:28:52 GMT  
		Size: 46.3 MB (46303484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9e4b28f4c70b491bc425ae0c0b8fc849fc3a59ff25d3efa2fb9cf1a9bc76e6`  
		Last Modified: Fri, 14 Nov 2025 00:28:54 GMT  
		Size: 82.0 MB (82009642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df04f27e6295adef6bb6401f0ec49a56d23f939eb1e2cec9249cc69807c93d9c`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba64dc4b68645941b6e163791183152612fa0ebc92fee387fd4660750cabaa`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:01cc88792432f43c356679ae274fef28b207b3c1240b69c9dc3fe010ad2ff4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e95c87a147a28fed5df5662afaf5075e693a74b2b61815a98c2a2f78d7286`

```dockerfile
```

-	Layers:
	-	`sha256:a39870c15d12b577e34cfbba53326926f1c47027f4ff66efd70517a8a6e9b525`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e700bf823a01ee7b340e763219eb84fc053accb5b66c1ea64c45a2553bb236`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
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
		Last Modified: Tue, 09 Dec 2025 03:43:48 GMT  
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
		Last Modified: Mon, 08 Dec 2025 03:44:37 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:7fa702d2444080c86ba6b0733286a7324800b4c0faa3177349b4852d7f93602a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:ad424b6437336383d6709f715fcc4d07447a25631933fff8ebf822c8b822ccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173104505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fcb0d2a2b24d7a2375a04baa29202f7c1dd9161e1024061225fc72f3b24caa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:08 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:08 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7135dbac77e480e19f2fab49d6bf449a7b00e25043f30204f2c35cbaf2081e`  
		Last Modified: Fri, 14 Nov 2025 00:28:35 GMT  
		Size: 48.2 MB (48248227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4667606aa22066eb1ead38518f235c333ee2336fb3ca2ac1e9be16644ca7e4cd`  
		Last Modified: Fri, 14 Nov 2025 00:28:41 GMT  
		Size: 88.2 MB (88212738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82416f38ec3797f036f93179be2ce2564f4204507898f04753b75730f39d8da1`  
		Last Modified: Fri, 14 Nov 2025 00:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de306879312a1e10fffc2828bfc33198774cbaaf6d943b4ff63f9ffa63c7a639`  
		Last Modified: Fri, 14 Nov 2025 00:28:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a7da07e90eadc8945c1c0cf7649e29a39ab734e3a29ad19d3018ec47d2c599e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a54ded414376942e7256e72a433b9d8afcb21ae4aecc958a903df8836ba5003`

```dockerfile
```

-	Layers:
	-	`sha256:4cba04e58c70efe1eba618345ae547556183fc88c902756df7a4c8c3928c2438`  
		Last Modified: Fri, 14 Nov 2025 02:21:57 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07e8b3b981f40dab492441333de3d022e7c2be22df664e320c2b50065dbe332`  
		Last Modified: Fri, 14 Nov 2025 02:21:58 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d0d87f6e0e8ae3377d4dd02dde6bbbcfedbda40aacf90bdb018ff091f604e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162750022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d05fb9a6cec856b762b1711ec4b5346c0d92050196a6152c416247d87409f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc514c00b5880177c45acb158773e3e0427cbf47b9e3ec5fe3976be52704a5a7`  
		Last Modified: Fri, 14 Nov 2025 00:28:52 GMT  
		Size: 46.3 MB (46303484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9e4b28f4c70b491bc425ae0c0b8fc849fc3a59ff25d3efa2fb9cf1a9bc76e6`  
		Last Modified: Fri, 14 Nov 2025 00:28:54 GMT  
		Size: 82.0 MB (82009642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df04f27e6295adef6bb6401f0ec49a56d23f939eb1e2cec9249cc69807c93d9c`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba64dc4b68645941b6e163791183152612fa0ebc92fee387fd4660750cabaa`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:01cc88792432f43c356679ae274fef28b207b3c1240b69c9dc3fe010ad2ff4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e95c87a147a28fed5df5662afaf5075e693a74b2b61815a98c2a2f78d7286`

```dockerfile
```

-	Layers:
	-	`sha256:a39870c15d12b577e34cfbba53326926f1c47027f4ff66efd70517a8a6e9b525`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e700bf823a01ee7b340e763219eb84fc053accb5b66c1ea64c45a2553bb236`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
