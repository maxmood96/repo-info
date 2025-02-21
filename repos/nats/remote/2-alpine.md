## `nats:2-alpine`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
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
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 19:16:02 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 19:16:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 19:16:02 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 19:16:02 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 19:56:19 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 19:56:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 19:56:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 19:56:18 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 19:38:54 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 19:38:54 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 19:38:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 19:38:54 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Fri, 14 Feb 2025 19:50:30 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Fri, 14 Feb 2025 19:50:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Fri, 14 Feb 2025 19:50:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Fri, 14 Feb 2025 19:50:29 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 19:43:17 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 19:43:16 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 19:43:16 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 19:43:16 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 19:45:02 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 19:45:02 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 19:45:02 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 19:45:02 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json
