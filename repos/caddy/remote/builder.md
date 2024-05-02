## `caddy:builder`

```console
$ docker pull caddy@sha256:9431b9be7b427f276ba717cc590fafedf6018b04f970c04fa13649e8aed42dd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:9244610bee53db8b191c73639ea976486483f2d04d9d1e13dbeae01b3dfeae8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b990867c3b116d81aab3cbd4b61eeaa131ec4dd8bc711bebe9910e98c74281dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOLANG_VERSION=1.21.9
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOPATH=/go
# Fri, 08 Dec 2023 02:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 02:23:07 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /go
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ea484d3a61a4018c1ab90a6775f67a209314a57d525171a5a269d9302c191`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 5.0 MB (4972832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052cb73c4ac7d917c667d29f8d05569d6aa87db3508e56cfd0debe538c73a59a`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.3 MB (1302224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285220af43cda99757c2e7399af861f21d6d5c9eb1e0fd830b3042d75e506996`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:fa0dbcad8f7cac8cca74c1ace9d303f584f6d96bfee8152976f2ac531112ee8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 KB (283388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df938034dddbb7e7f575a1449807689da7e0d22f7b9d8f8dc7a49b5846ab9089`

```dockerfile
```

-	Layers:
	-	`sha256:440d384fa5e5796039e585cc11f7594719facb3722c8f256c77984628bf2bfda`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 263.0 KB (263046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca400870f0d05d15d01f6657557cdeea948c97e6610f185d21b7cdbd86930bd9`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 20.3 KB (20342 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f15c5ddef0e06765f11ace23b39847745fdb2900e7c53e3262707c059a25fd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff567d8839681c40ae486b0d77bde7dc64a9a8e7d498514d36f9bf0b025a31d8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOLANG_VERSION=1.21.9
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOPATH=/go
# Fri, 08 Dec 2023 02:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 02:23:07 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /go
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc841f1671481b5c9adf49d6fb699292c1f49fd811998e08e155ea8b0d5fb641`  
		Last Modified: Wed, 01 May 2024 21:56:33 GMT  
		Size: 5.0 MB (4958575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ec89aec4329a71a89bfcc374e6caf1e2b389ea73e75e0ca0975902cd62ca4f`  
		Last Modified: Wed, 01 May 2024 21:56:34 GMT  
		Size: 1.2 MB (1248630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da2028b82d567c0598a8441cef0052773dc99abad120b1d76cc30e2ec591f9c`  
		Last Modified: Wed, 01 May 2024 21:56:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3bd24b3e2fae272feaba8822dcca87f05fc36037d883117bcf08d745dfe61868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac269e272105e2d85e1e2c7b009109204b3e4d87bcc432acaa6e386f8777814`

```dockerfile
```

-	Layers:
	-	`sha256:6f87737d8a34032ffcc7833277ec062826e30e72c8aec3852f090cca3bda3a66`  
		Last Modified: Wed, 01 May 2024 21:56:32 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5389fabe9016869e884ef097e2ad6505855b4ba62cbc2f035c0062cd68ae1762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d867a81d133afaa2c668580ad60d7f0697bc21a4c0cfb012e6d318c966263ee4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOLANG_VERSION=1.21.9
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOPATH=/go
# Fri, 08 Dec 2023 02:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 02:23:07 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /go
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0710a2201c8dfbd879549e95d5281a43bbf0278c2eb41b4aa51099afbbf268af`  
		Last Modified: Wed, 01 May 2024 22:06:33 GMT  
		Size: 4.5 MB (4514399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f30e1931d96d49758e6d78a2277bffea3e2f151de2b77e1f92fb7f0d114519`  
		Last Modified: Wed, 01 May 2024 22:06:34 GMT  
		Size: 1.2 MB (1246059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1262f7783e37212e5112293fe39dce41912340a52bd4ac06ad799d6cd1b4c212`  
		Last Modified: Wed, 01 May 2024 22:06:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3d51066eecb29d95fca0a4def3aa8b40e3f2307d0a36270f8a8a65399fe80cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 KB (286119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11b9e5ea7626826fe07c1a7147e4797fef13722fb73a07462763bb9192d07ba`

```dockerfile
```

-	Layers:
	-	`sha256:52df8dcc828806a5c23f4fd2a19971842f7ab4b4fdd6fcfa08ffcd6714f6d160`  
		Last Modified: Wed, 01 May 2024 22:06:33 GMT  
		Size: 265.7 KB (265662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2e886685275e22bc3adbae69ce140e9e681dc8a13c52512ea4cc648ff98784`  
		Last Modified: Wed, 01 May 2024 22:06:33 GMT  
		Size: 20.5 KB (20457 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0a05be6a5db192f59e9c1f8dbfdb2b94d6edd0eac7e93aa9ae7030e8d7f43869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc52e8585dc9e2a0189ca01cb9ef099ca291b09cd1bfc6ac59dfa1fa7085421c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOLANG_VERSION=1.21.9
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOPATH=/go
# Fri, 08 Dec 2023 02:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 02:23:07 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /go
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfddb6e41141613b991a0cd3bfc8b36545549745d3fe506115e54a77d4a49af`  
		Last Modified: Wed, 01 May 2024 22:23:37 GMT  
		Size: 5.1 MB (5063861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d1bda7654387495717d8c3a120616e4aeae44ae28103c74222f68089b7a1b3`  
		Last Modified: Wed, 01 May 2024 22:23:38 GMT  
		Size: 1.2 MB (1198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0968a193327750b2f750563712297e119d9c1d847e9f1358d665ce21e8192`  
		Last Modified: Wed, 01 May 2024 22:23:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:fac300c26e5d7fb65728a921661776854273dd0ac9f58705aa63bb4a75e1454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 KB (283425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44b1e598cd2ea8bc3a5588035a6d1016bdc855e88fe2900902fb377c0bac78d`

```dockerfile
```

-	Layers:
	-	`sha256:2630f419e594e5099d9c856729d807c6f633a0725b88f4e8e528c5bc285ad559`  
		Last Modified: Wed, 01 May 2024 22:23:37 GMT  
		Size: 263.1 KB (263065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898289de181108d797d732522fa8e361e05c2c9355af7eed1caad3848a5ba3af`  
		Last Modified: Wed, 01 May 2024 22:23:36 GMT  
		Size: 20.4 KB (20360 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:fee2111aaf4015c96ce0492416c398cf517a5cc203f249f4f5101d2994c9f64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddde0e25b81824539b5feac105c47108e3b9f3f3c38ef6dac67fd630e6e970c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOLANG_VERSION=1.21.9
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOPATH=/go
# Fri, 08 Dec 2023 02:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 02:23:07 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /go
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b19414f7ddb6706499fc60fcb1f2d4a3ab8248d09aadb518cbe33da92a85a`  
		Last Modified: Wed, 01 May 2024 22:08:16 GMT  
		Size: 5.3 MB (5270894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c54cb0aaf6d33526e44dbac07af1810d473849a898ebc23b3a6fd2a7c8f303`  
		Last Modified: Wed, 01 May 2024 22:08:17 GMT  
		Size: 1.2 MB (1186175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f4af4b9e0e09a0d2c5cfb6e3d73b9c9113df62b78c5803a38c46deeab07593`  
		Last Modified: Wed, 01 May 2024 22:08:17 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:5a8b29b380d394e252d9fd9e94823df49fc961b24770b01cbd2339f6a3fdf719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8716fa3a86581d5cb7115ee760ab3520979ca4cdac3918d7cadeae709a4857c2`

```dockerfile
```

-	Layers:
	-	`sha256:f07a67ffa3209cf539f6596bc31d6ce847689062e84274de8b70bb18500f4afa`  
		Last Modified: Wed, 01 May 2024 22:08:15 GMT  
		Size: 261.2 KB (261184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d1b3f2d904bd9534dbbfb7b4a8e7a780000bdb32f834c88012c25637e69d52`  
		Last Modified: Wed, 01 May 2024 22:08:15 GMT  
		Size: 20.4 KB (20406 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:40792d4f88a22435faeaf751eee59482395a76f1aa4c27e8006ceb065c142c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcb7ee45640e3f34a591367e907e98e4ddb96f5f07d95a05c54b8e89b9545`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOLANG_VERSION=1.21.9
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 Dec 2023 02:23:07 GMT
ENV GOPATH=/go
# Fri, 08 Dec 2023 02:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 02:23:07 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /go
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78262269f425e8a29d427d379b2e71ba674ec34205fbc7930dec94511b882cce`  
		Last Modified: Wed, 01 May 2024 22:06:47 GMT  
		Size: 5.1 MB (5117169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e733f27719eedc3fd4d89f81a6347e50064f211c61d07ddd7455a9f35116527`  
		Last Modified: Wed, 01 May 2024 22:06:47 GMT  
		Size: 1.3 MB (1262365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752676edfbed45651997851d54ef366f352c1597dfc20a44cf0b6540ca9cdcd3`  
		Last Modified: Wed, 01 May 2024 22:06:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a6df7431012e0d1f5f70605ef71cd8eb0f7878f1ef8123e445612c3f6d72f9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd27558dc11c913aa7d087c53820d6743aa8b5f6848682fee45d2b99631b20f`

```dockerfile
```

-	Layers:
	-	`sha256:1af423e9269665fc0efb1d856bb0f1e56202e55a748b55665cd9f366b700305a`  
		Last Modified: Wed, 01 May 2024 22:06:46 GMT  
		Size: 261.1 KB (261090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0076544bf5ac03635f4988f91726433927fb770db7c16b85c2a313a342cdaf`  
		Last Modified: Wed, 01 May 2024 22:06:46 GMT  
		Size: 20.3 KB (20342 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:9e173a276104128d86b3d895dcaad659d849dd38390acfadb4474ab678143707
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096224959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c43933ca38ad747742f667f45d13c85f7970e758834afe474351fa314b8e819`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 01 May 2024 21:53:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 May 2024 21:53:46 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 01 May 2024 21:53:46 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 21:53:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 21:54:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 01 May 2024 21:54:17 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbd0a9d9824a6d9c2500ed3ee6cc3567767e6fc9d8d8bd590673bea601b0f56`  
		Last Modified: Wed, 01 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de375a9434a50615349bd0ff8bd370eb1a54f509bc8aa4a18cca94b51b0c7eeb`  
		Last Modified: Wed, 01 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87b203f0d3c89b5c55f2e09d3ce253aca1b2f726996de11e8ec71fbebfe8cfe`  
		Last Modified: Wed, 01 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48c644cd59573885114f335416fb30eab7e3c8cc422f1f92337e58cb2bf40c9`  
		Last Modified: Wed, 01 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378897916f53f45f02ca10ce246acc9e53c7d654bb3095d7f247d535abb6e8ab`  
		Last Modified: Wed, 01 May 2024 21:54:19 GMT  
		Size: 1.7 MB (1709499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bef088188eda203d722f2909cb535d122ec65200d10bd5ba74893a094aa0b9`  
		Last Modified: Wed, 01 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:ed8fc1932352ce2acb9f596b9f4cbfb32e6b38ff8323ddbd36064a4da378a764
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261324573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40283e1c1bae46f57a0e3ac59b4537e1908f6f863330b35a96726738460ffb7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 01 May 2024 21:53:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 May 2024 21:53:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 01 May 2024 21:53:15 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 21:53:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 21:54:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 01 May 2024 21:54:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcb71d349df8fea0c1cd07402f1714c6acd89ef121eb4882dd42b04b03eb1c1`  
		Last Modified: Wed, 01 May 2024 21:55:04 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d7de0a64d6e634296efb783e5136760add0c85f7b6c0f1d57ad7bcbeb576b0`  
		Last Modified: Wed, 01 May 2024 21:55:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3563f8c08909dd6f0d292741d738f23b2f8befbaed817bc010c3e3d500b786fc`  
		Last Modified: Wed, 01 May 2024 21:55:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3ab914dc15fe91331969744948030394957dc398a1bf317a626f62eb5e580e`  
		Last Modified: Wed, 01 May 2024 21:55:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632814b445d056fc796d0017902587c1c98929634ced141f4f5ef930184a4df4`  
		Last Modified: Wed, 01 May 2024 21:55:02 GMT  
		Size: 1.7 MB (1728394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f7d959854b19ea0bf9de1ce27113e4e61c85a0296044763b30ce5c76226f4e`  
		Last Modified: Wed, 01 May 2024 21:55:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
