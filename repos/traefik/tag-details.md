<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.35`](#traefik21135)
-	[`traefik:2.11.35-nanoserver-ltsc2022`](#traefik21135-nanoserver-ltsc2022)
-	[`traefik:2.11.35-windowsservercore-ltsc2022`](#traefik21135-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.7`](#traefik367)
-	[`traefik:3.6.7-nanoserver-ltsc2022`](#traefik367-nanoserver-ltsc2022)
-	[`traefik:3.6.7-windowsservercore-ltsc2022`](#traefik367-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.35`](#traefikv21135)
-	[`traefik:v2.11.35-nanoserver-ltsc2022`](#traefikv21135-nanoserver-ltsc2022)
-	[`traefik:v2.11.35-windowsservercore-ltsc2022`](#traefikv21135-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.7`](#traefikv367)
-	[`traefik:v3.6.7-nanoserver-ltsc2022`](#traefikv367-nanoserver-ltsc2022)
-	[`traefik:v3.6.7-windowsservercore-ltsc2022`](#traefikv367-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.35`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11.35` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.35-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11.35-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.35-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11.35-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3.6` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.7`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3.6.7` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.7-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6.7-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.7-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:ramequin` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.35`

```console
$ docker pull traefik@sha256:ff7931742cdff6df8410aa1c3419a9e81ed7a983b866b781c4628088cf95110f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11.35` - linux; amd64

```console
$ docker pull traefik@sha256:6b35e53e362d4a4fbc30722e1eb44738112ba523be34362f572fc54a30bf816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51040794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed20dfb085f1a0b3a6732d14f91cf286681d2b42d389150ca29ec4347b71b1d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e99a0394b9a0851d2887c994def86f93b24f2f329e12866234ca82194140b7`  
		Last Modified: Wed, 14 Jan 2026 18:05:04 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde696496f585722602dc125ee19dfc84376abf430bebeded1513756df79250c`  
		Last Modified: Wed, 14 Jan 2026 18:04:58 GMT  
		Size: 46.7 MB (46719369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b4be18136fa4057ee399abe0a6439aef777b70fa9dcac9ad1bf0b0b8f4767`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:d2ea03988cd2c541e914c0aee12b4bfffbf9eec3c99a6d2fe8dffdde13f11ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86a159982d39c95d1c5dc4b71343331a870df99bc4cf06a820afbc6918cd23`

```dockerfile
```

-	Layers:
	-	`sha256:042e523a939198d046090328abb5fa60e3636311936ef26e23be9feef868d965`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5fe64469a02872b71a78323ba41f56f6bc524a87ca4e59564e76cad4e211`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dc92974ce996096cb1a3862411c132a53f0db3b9ba54a83f9cb945fc3e7e6189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9292eb3041b60125bab8f6f62e08634ad16e3691771483803ba8122b8febc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:43 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf020733d348c7dff7dd641c7bff46b268031e361991c79fae6c0f5fba3740`  
		Last Modified: Wed, 14 Jan 2026 18:41:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216efc9f7bd6fb58aedb133544afc07c77df02cb2ced151d68ac5ff131a6ff1`  
		Last Modified: Wed, 14 Jan 2026 18:42:11 GMT  
		Size: 42.8 MB (42792501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00f42c2d74790ed5ecaf84bb10101c52508f3e97d29c84189b4fd11b433e0`  
		Last Modified: Wed, 14 Jan 2026 18:41:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:9508d7a2f3f58ca98968c3ea9617fef400c9bfa3461d49a0de901b182baad116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deb681cfcdb5ecfb6a15e9347e62fe3e8819c39345be4e5095732252fc56092`

```dockerfile
```

-	Layers:
	-	`sha256:ba12cccda11707ee657d6d676c0cdb04498946b34b34b2e52e310148ee140071`  
		Last Modified: Wed, 14 Jan 2026 18:41:52 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:df4488969fe0c16eb3bceb131d35982b2cec7c9142545057b329bf62078d873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92418a7a13b8d6e79ed355e1b1ef908066665e777707c467e941313cdb58437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:59:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:59:13 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:59:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e4be29c53ba53ee8029d05a4b01b94783d70d70ccc5939d4534fa53d7a085`  
		Last Modified: Wed, 14 Jan 2026 18:59:57 GMT  
		Size: 42.6 MB (42622293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a502c9bfbc6e4c0499ccb28b745f76db46a3a069a176dff302650cdffa0f525`  
		Last Modified: Wed, 14 Jan 2026 18:59:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:84cecba66d721be248618438af0a247690a2f0e04bad1efac16fa95ec71afcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc8b2eb4b13515c77d125b2818b208998cd9cc33c51e24a27f9a0ff0b9f4b7`

```dockerfile
```

-	Layers:
	-	`sha256:1c633be44ed6ece977e0b048d0c5089bbb0b0789e684e4fc672bf5af6a5b0d47`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de524513251da5a9c378262826ddeae7cb49afa0709b84c3e0a6dde5e0cbb2`  
		Last Modified: Wed, 14 Jan 2026 18:59:38 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa69ed9fde95f3cb6d437a34b40028ce94704c3bccefbebbfde491a1ddd652b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45244550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7d1133dd79ad9cb7db249b5ad724d5d4bf9d9525fda287fb5769ef87134910`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91da93e583d0c14df595cd3c551d7c0e0ce81cc706582371a003893644b7e5`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.0 MB (40952915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f705d647b0b457b48a722dca900d7d57e544ce54a66188e8716fbcbd49a13`  
		Last Modified: Wed, 14 Jan 2026 19:01:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:a92e3cd53b17405edea5766b1ad5b153ffd332be9bc4a31080bf1bbf3eb1b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e229fc3192b49e9a13354a24bdabbf5723a46588037770155ef0b20d4ccc29f9`

```dockerfile
```

-	Layers:
	-	`sha256:08b5553658778d4af8c7d76f09b7f0d7da40abe2bbc6934d6d506ef0db1bfd46`  
		Last Modified: Wed, 14 Jan 2026 20:48:18 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea63ed56a73bea2721bbc1f6f6b4b98dda806f60dac2fa417db19fbb8b4ee3`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:45 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; s390x

```console
$ docker pull traefik@sha256:d1ea3bf224942427fa9e3552239ef3948841d3144a73add95f6a3edc4b6fdcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f71be97aa2d38828cc1d77476c16eb0eed22bb4b646452bde2b6eef091c2196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:15 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:21 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4770eef3c695dc5d5245a388c3700aa7f1b90dce08cc3dfd5ec2e155a9629`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 461.7 KB (461739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf747e04f06e7c34857c4c99277054f8b7317fd3829a650683a29e0858d28fd0`  
		Last Modified: Wed, 14 Jan 2026 17:58:23 GMT  
		Size: 45.2 MB (45248296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcc853dd2d0d6d499ad76e981ce05ec56967819ec3290ce6f7dd6062c82aae`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:a845d82b54542735b63531ad8345c984750183529cc5bb2fa42cd17643958cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e669ab1edf60dad4494bb49650121d0e46132392102768a6ee3b8228c2e71`

```dockerfile
```

-	Layers:
	-	`sha256:3ddcdb7a683cef301f63e992e6b8f062689bfc8990459911bfde1fbe58d18e42`  
		Last Modified: Wed, 14 Jan 2026 17:58:08 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4188c351f867b0c86b5cccf415e2332f73c41b0614137dab27a9f785e6b9c2`  
		Last Modified: Wed, 14 Jan 2026 19:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.35-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11.35-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:48:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.35-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11.35-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:15:42 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3.6` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.7`

```console
$ docker pull traefik@sha256:ebe7d3fc715e28f033cea8265e9105b9d64705867f5b916e2d9ed0b62c530192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3.6.7` - linux; amd64

```console
$ docker pull traefik@sha256:4aa7b9c53ef15139990a6244a0804274f48242693b5029e63eacaea7e1557028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52178755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171247bbf2d7096d7f4ef2d64b3d65275886540d8fbf919b27f559d202c1960d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:04:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:04:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:19 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:04:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95a56714d06f70ed647a81052152f5070071a6eae8ab3ba388764d7d9bd67d`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 461.0 KB (460961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b4f5b88cf886b71b0fbe422a06969d838554e63bcbe20b4771101a687ffd7`  
		Last Modified: Wed, 14 Jan 2026 18:04:57 GMT  
		Size: 47.9 MB (47857320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56045ec5f13cd9e1781dafe3830c189b79fb35842fc53691c481b39fd16fd586`  
		Last Modified: Wed, 14 Jan 2026 18:04:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:b62d20084448541945ad46a1fb3bbe7152d38e658b5430692390fc755276bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775b6433adce3b1cf7fe8203bcb70c0078f44e462f569f9b2e0e60377559ba5`

```dockerfile
```

-	Layers:
	-	`sha256:abcfd388c08b0a231604c715c76d785b1249b3b1ef0738ef4680301d83a6c8db`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936003e86d4164d245189600e91ee4326cd1ba8b6493a5a438b9df38ac45bba`  
		Last Modified: Wed, 14 Jan 2026 18:04:41 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7224d6f5147d82964f59a4758fd65bdfc1fbc74405848e8f4cabbad361c9416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47436149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec432e933720544400d0fcc909f5b351f3ceab61784b3464a3d66be5b442d178`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:41:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:41:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:41:24 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:41:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8891c6ebcb306346601f1d4193f47ab8339ca58b77f511cca8a9933a5a9662`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 461.5 KB (461452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125b9420f5371d048e5bd1f7cf4a669c9ecc7610dd002f637e16b60c3d18acf`  
		Last Modified: Wed, 14 Jan 2026 18:41:35 GMT  
		Size: 43.4 MB (43405896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36ec7e764fa9724b873b619bad9a5b30982aaa4d2e54d2b5be78d39471cfc3`  
		Last Modified: Wed, 14 Jan 2026 18:41:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:0b5cc28cf5071d9cc8bb1c2ec00f26aff03a8b1e4511f809d5a8637a01a60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d372e4416593fab3f6bdc882c891a9fd884d4f44da6674fa0eb6a07650f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:dae39b6ab79b3eeb24e34696eb3553b53d98fcea3950da760c9709edd13429c8`  
		Last Modified: Wed, 14 Jan 2026 18:41:32 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a8e2f8b0eb3d81b843b8d5a21024bffd6052b6c8dca4565855029ac4551a1c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e05d777f3e1b962443eaa28c6c8fa50fcad79ef94b02a8a1fba5cfb260a24c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:58:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:58:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 18:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 18:58:32 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 18:58:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b021a230d066c2186eb3cadcce518a71a7ec2d6eaf491ef0ee9d79f84b4dbb9`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14d4e4580ccacad3a4f88170b6e953ebbf36144f544c0643c230c848659296`  
		Last Modified: Wed, 14 Jan 2026 18:58:59 GMT  
		Size: 43.5 MB (43459944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40033e303f2e178b3a85d8922e59fb883048c43e614e331e13a28db916860628`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:eb498da3e4043ae1e0c96399b5fa5b97d17a350022a5d568dfd0d94f597ecd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7515aaeebf613c688348baa1102a817b31b3260d5e8511142d57fc2bec676a`

```dockerfile
```

-	Layers:
	-	`sha256:4e888f672bff491b47e41e2cd12903b2aaba20d6c424fcc91e16f1ffd61f6a4f`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda17e18aeace49f719a44039c85c1fcc1076d45a0c029e473f3a899758a6c9b`  
		Last Modified: Wed, 14 Jan 2026 18:58:58 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6596a6eb964a997744cb31947663de4252febcac599ebeb4e625df47a21e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b7683695547cbf412cb3ff1ab0433c05d72666fe4cacb473d3bec6efa796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 19:00:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 19:00:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 19:00:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 19:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 19:00:12 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 19:00:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb78553d8b7269d09e6174fd249797902dc9e6654628b769015839ed159632`  
		Last Modified: Wed, 14 Jan 2026 19:01:08 GMT  
		Size: 463.5 KB (463512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20235d61654822aa820aff3981ac2537223bb8ce42c51cf17b0bd446b5dbc242`  
		Last Modified: Wed, 14 Jan 2026 19:01:09 GMT  
		Size: 41.3 MB (41304986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff34c27ce69272a2b9fa3c44271f8cdc1b01629b900fe8ceafa2c985c376c0`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:c7e1ae5c09aff754a0f0f3be2c2e1f3ff1e5663e745fd99e09abd3f1b2a3a9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22c54893b79e0262b1d71bf58ce0c9a74c0850a56abe3136f3ebd6a479eb32c`

```dockerfile
```

-	Layers:
	-	`sha256:482260bc38880da68204f02c7090fde18584b9a456fbe281585f082635867176`  
		Last Modified: Wed, 14 Jan 2026 19:01:07 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43782000a11b6834def09f61367c475f1a258d3dd95dfb7a0b807188c4bbfbc`  
		Last Modified: Wed, 14 Jan 2026 20:48:11 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:37 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; s390x

```console
$ docker pull traefik@sha256:329dbcf91f24669f313d399f74d411785b1e8234dc80598ffc02145fb29bf100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da091deede5b7248dfba8cced60d3b7bad5b372872c98eb0ba4094bb692f915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:55:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:55:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 17:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:07 GMT
CMD ["traefik"]
# Wed, 14 Jan 2026 17:55:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee7fd0c3dfa8390f7865fa22896a7d34faeecfb939c43872c0002f60c34a07`  
		Last Modified: Wed, 14 Jan 2026 17:57:50 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf404becf9294e7042a53689a61fa8af3762b06dcd2060ad321ee14fed8a56d`  
		Last Modified: Wed, 14 Jan 2026 17:57:44 GMT  
		Size: 46.1 MB (46137593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816cde01ee4e70afefd262f1cd9a065b0160ed7e72e60248461df986783a6432`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:43d6bc031cbcb4d9a4fff6a19a4a9667626b498174650759701618c9986489f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a8dce813cdd05b8e2bcc31c09385859a156a182d3677c49f693a7471950ac`

```dockerfile
```

-	Layers:
	-	`sha256:4e38c2f2783d5f58058c3c38df5d353d388b59b58e142124eb22cab59b500227`  
		Last Modified: Wed, 14 Jan 2026 19:10:01 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6139bede29097e6f8cfadb7346dff83a336241bf5be8711914294f373ae51d`  
		Last Modified: Wed, 14 Jan 2026 17:57:23 GMT  
		Size: 12.8 KB (12764 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.7-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6.7-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:42 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:46:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.7-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:13:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:13:13 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
