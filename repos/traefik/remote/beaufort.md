## `traefik:beaufort`

```console
$ docker pull traefik@sha256:366c8d828bbca39618b16f40d1778e1d3ea23add991ee75cd3c61e0e5eda4322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:17d3db6bb6c7eccb2bb3010fb9bfb0f5d86612538b4b8628b5209ac2a054ec81
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47438078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4ac3533e1c60deca72044e6b65a5ebb88cd20541bb52e99436e1ad18752d68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:51:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:23:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:23:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:23:32 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:23:32 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:23:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d5da2188cebebb3201442bac5e2e392e8ddea062e25cd77ce17d63272a4ba`  
		Last Modified: Thu, 30 May 2024 19:51:53 GMT  
		Size: 463.2 KB (463226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedcc51844aed35ae51d3b58ce4dc6896f65bb8baf74e6f2bc67eec07a83769`  
		Last Modified: Tue, 18 Jun 2024 18:24:01 GMT  
		Size: 43.4 MB (43352389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9053df3070e0188cb9bed31983b0bebad39fb8205859970ff937be9393903f02`  
		Last Modified: Tue, 18 Jun 2024 18:23:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e33fe33f01c78ea3c1bf25b58c29ae07276a811626e9fd6189193b9c5e0f4a6c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44478986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618668e9fcb1b43be56268057a8f9924a353548b9d44d8493f08b9ae6e2fd665`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 10 Jun 2024 21:35:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.2/traefik_v3.0.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 10 Jun 2024 21:35:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 10 Jun 2024 21:35:27 GMT
EXPOSE 80
# Mon, 10 Jun 2024 21:35:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:35:28 GMT
CMD ["traefik"]
# Mon, 10 Jun 2024 21:35:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e0d37fb3a3fa24afbe2e75b8b155456fc23029b9d964091885b19c431ca1fa`  
		Last Modified: Thu, 30 May 2024 19:49:57 GMT  
		Size: 463.9 KB (463909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e382a805c0902b2319c01a743f03948c5934c72f8c617011e19523505766d70`  
		Last Modified: Mon, 10 Jun 2024 21:35:59 GMT  
		Size: 40.6 MB (40649654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1195bd175a13f8dd20b414e164fa0bf60acbb53132dc2c7aa1a5b55d8e91a50`  
		Last Modified: Mon, 10 Jun 2024 21:35:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fc2e6b328a8dd0b21392f9ef3e124b0f6bfc0825ecec3a6acf3e489b4d7b0102
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44716641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42aebebc29eb7c93427d07b13e1e5753477c2f8d27a8c1908e21a66ad20095d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 20:43:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 10 Jun 2024 21:46:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.2/traefik_v3.0.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 10 Jun 2024 21:46:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 10 Jun 2024 21:46:30 GMT
EXPOSE 80
# Mon, 10 Jun 2024 21:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:46:30 GMT
CMD ["traefik"]
# Mon, 10 Jun 2024 21:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33761638787616d48b5555dabc2c016480383aae25d9242a7b093c7e0b660e1f`  
		Last Modified: Thu, 30 May 2024 20:43:58 GMT  
		Size: 465.6 KB (465576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b153cb02af97772ee491de03f67c61b8426bede1efe005023d4280fa3e83019f`  
		Last Modified: Mon, 10 Jun 2024 21:46:55 GMT  
		Size: 40.2 MB (40163921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481da11acf179bd12e47fe63827abb5a5d3bd5d6d34d104dc22f12a34b80d3ab`  
		Last Modified: Mon, 10 Jun 2024 21:46:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:7058a434749dd0134b783504284a98896b82868bb3102d88647e2928c86d592a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42991876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a344c9bdb266525a94ae7a964c19b8485c753bf267400428fcd6d553ef829c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:29:22 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:17:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:17:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:17:07 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:17:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:17:08 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:17:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d99d4223e6b15fb67e3b010c6a956226b520efc8dd99c401d67aa092943715a`  
		Last Modified: Thu, 30 May 2024 19:29:56 GMT  
		Size: 466.0 KB (465958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e18f816e444cd23b4d95f2d93c5179bc8a039ae837472972bbb1feff1afc4`  
		Last Modified: Tue, 18 Jun 2024 18:17:42 GMT  
		Size: 39.0 MB (38955704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c55882a212d56b7a6cfbe0d4d8c590eb9bd231ef411ce4053487ee284352469`  
		Last Modified: Tue, 18 Jun 2024 18:17:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; riscv64

```console
$ docker pull traefik@sha256:197508c9b39228a11a47a1e7d52498190c5a558c9e25a055faff966469771cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45755555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f44c677311986d55fe7bd622599cd745eec1369cc2969562edffe20eb06e45c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 18:24:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:18:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:18:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:18:51 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:18:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:18:52 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:18:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d47e1f3d311b4fba413e02ace3d5493b4e73c7e4f7292210a16e03cf783b0a`  
		Last Modified: Tue, 11 Jun 2024 18:25:42 GMT  
		Size: 463.8 KB (463827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c877525b1cf46125d7510a6e6f1f18cd4000ca7ae5102aacd1b3d6b934aafa72`  
		Last Modified: Tue, 18 Jun 2024 18:20:35 GMT  
		Size: 41.9 MB (41922799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594120322406377272966311259df2b205a1336d71b8f8770f958e0c82cb855b`  
		Last Modified: Tue, 18 Jun 2024 18:19:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:3fe5e1982bc79e074fead0406e2e2eb9d2a696cbeb63e76c4ce19340689bf0d7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdbdf7fb0803d3e834355d99fe9f7717435519ade96467274c8a299221a9b6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:44:18 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 10 Jun 2024 21:32:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.2/traefik_v3.0.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 10 Jun 2024 21:32:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 10 Jun 2024 21:32:44 GMT
EXPOSE 80
# Mon, 10 Jun 2024 21:32:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:32:44 GMT
CMD ["traefik"]
# Mon, 10 Jun 2024 21:32:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfdae686589931bbb09e116bfbb8ee205184c76b0a1158eedaa6d28ca76f73f`  
		Last Modified: Thu, 30 May 2024 19:44:53 GMT  
		Size: 464.2 KB (464183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82d41ad15f6f2841805379e8599df09abc339b802f66178d32067172aafe49`  
		Last Modified: Mon, 10 Jun 2024 21:33:28 GMT  
		Size: 42.1 MB (42091546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a419ce2b3e340588ccf013e18e406b82bd764fe195d5931ffcfe80f93a3f3af`  
		Last Modified: Mon, 10 Jun 2024 21:33:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
