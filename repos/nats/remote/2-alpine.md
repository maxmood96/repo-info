## `nats:2-alpine`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json
