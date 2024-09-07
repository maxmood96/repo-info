## `traefik:comte`

```console
$ docker pull traefik@sha256:e325efe05922db1a4fe8b026a57c07ef65254efc5cd8ad5ffec767d8a1b34f0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	linux; s390x
	-	unknown; unknown

### `traefik:comte` - linux; amd64

```console
$ docker pull traefik@sha256:b0e9f5776825144921e0f5ff77fa387f157a056e3e69ca7c13ee9747477041ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48575937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c02a120479c5db9809725d9bf5b125ffbc79266e4e6dc1e5225bff876880453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 06 Aug 2024 14:12:12 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 14:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 14:12:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86a2979cd09ed01bccbc77fff3f302c7238b66d94ecb24c5039a6832d5031c`  
		Last Modified: Fri, 06 Sep 2024 23:25:45 GMT  
		Size: 455.1 KB (455088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705aac0567c9dd6008342248da64e515100b897d99d3604f7c50c17fce77b23d`  
		Last Modified: Fri, 06 Sep 2024 23:25:45 GMT  
		Size: 44.5 MB (44496672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f907744fb759682800595df9d74c6b41ea87cd62cee56cc71d42b5e92bd685`  
		Last Modified: Fri, 06 Sep 2024 23:25:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:6687965580ed65b849e94ab89da19517be7d90dc15200450300039d382426aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.2 KB (805174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ffac02b921ae941d7a8c467658ab2d186f504ffe4e52ba0c264b9f926cc2c0`

```dockerfile
```

-	Layers:
	-	`sha256:b85e0d69775b7a740a8049d87bbe1a92796febda2fafff7106fb9ffd482d7afe`  
		Last Modified: Fri, 06 Sep 2024 23:25:45 GMT  
		Size: 793.2 KB (793186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80268254575b6cc850e4f0738f8ca0dd3e23b45e7a6723ce67171c8dadbe13ce`  
		Last Modified: Fri, 06 Sep 2024 23:25:44 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3da5a2fab6b3d9eeff317c18f2d01e341a097252330d10192301722d2f71a0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45379243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef3cc2e4b58b549447eef56bb658aad98e3eca219b588ad6a308a9e40246a87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 06 Aug 2024 14:12:12 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 14:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 14:12:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b198b4fc88f9f784e0d33686fd52862fdf1fe7e03ec4b3262dead44b2cff91a`  
		Last Modified: Sat, 07 Sep 2024 12:44:50 GMT  
		Size: 456.0 KB (456007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7466fdd47f0378dd29ac08fc93f685aeebe12ed846b2804efc3d02c3a6295`  
		Last Modified: Sat, 07 Sep 2024 12:44:51 GMT  
		Size: 41.6 MB (41556360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511a3342a03950816b09587d06e813a8bbfbc6d0b2241381fa8c4b11fe0ab7fb`  
		Last Modified: Fri, 06 Sep 2024 21:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:74223ed5d9d7c056cc46badb804c11f58cfa6ca0f3759bc0990fd5a1582ea6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 KB (11868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65974e647d6144908025937eccf0911a9c59cf00303793be3a009b06c6b90d38`

```dockerfile
```

-	Layers:
	-	`sha256:58b824e8daa352992782c6a3c0d5d506120f767aeda26c1da2392920e9cc8409`  
		Last Modified: Sat, 07 Sep 2024 12:44:50 GMT  
		Size: 11.9 KB (11868 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4c1d4304afcdc624af61d1ccb838bd829000b84cf334f1501882a4b382c2020e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45768855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c493da8579fa2304f90bcfe557e38755d5e63f3f99b52f97cdf9490998d54b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 06 Aug 2024 14:12:12 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 14:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 14:12:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bde25ae77dfbd6cffed88ba7353fc79feabd623f595950e292707e7b8f4fa8`  
		Last Modified: Sat, 07 Sep 2024 11:59:34 GMT  
		Size: 457.5 KB (457458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207d308ad743789562bada1b3bc0bdea2898060aa3a3f65a0c37d6bd3010e0fb`  
		Last Modified: Sat, 07 Sep 2024 11:59:35 GMT  
		Size: 41.2 MB (41223382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350ec52e8cc402910ff57d024b4289b1b8ccb4d40d151a9a96effe8bfe2e82e9`  
		Last Modified: Sat, 07 Sep 2024 11:59:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:145dbf347a832249ad8a5cf1da5c7921bf66e2aec9cfb1badfb379796e3ff2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.6 KB (805578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1943666b6c6aeb50e3e63dda8f72532c58576d4019f1480b0e0c47348e6d515`

```dockerfile
```

-	Layers:
	-	`sha256:e11d1154386fd7cf452f1c49cec0e6a00786aa054eef45f22106038ec5480ef0`  
		Last Modified: Sat, 07 Sep 2024 11:59:34 GMT  
		Size: 793.3 KB (793266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45777bd34183a3acd0d2bb2f03f7d69c499d30f772371212c804db657a2ea928`  
		Last Modified: Sat, 07 Sep 2024 11:59:34 GMT  
		Size: 12.3 KB (12312 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; ppc64le

```console
$ docker pull traefik@sha256:4b4d52142d428dd4f9349a7c12a12176f3a8f1636bffefe468cf6e8fd90de7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43807729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa7af545f9da33bde04930f2481ea238908664706e618ea6bbf84d2f63a0461`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 06 Aug 2024 14:12:12 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 14:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 14:12:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc224017e3f6b379d3cf001a2e97a7dc0f9f1f51148aae6a1e57d08c5929c5a`  
		Last Modified: Sat, 07 Sep 2024 11:51:35 GMT  
		Size: 457.8 KB (457847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fcbe8c5e9ec5c65f074f27f62a8ff46b361d702b52ac8ae37b82239203dad6`  
		Last Modified: Sat, 07 Sep 2024 11:51:36 GMT  
		Size: 39.8 MB (39777094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dbd98b1cd7375333e46b5cbef30f53f03dec872b8759864cdfb08de3873a2a`  
		Last Modified: Sat, 07 Sep 2024 11:51:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:9345d68ef9215b445a48f54dad4725d39e9bc424b719282af2acff540e95ea13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **803.3 KB (803318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b227e1a246498b9ab2b2682135e0543877540747397057afde353e84663e333d`

```dockerfile
```

-	Layers:
	-	`sha256:0611f402f8b924b43f6cbb4c484dd1ba5c21ed6e1b337242d28692d6345b0d6a`  
		Last Modified: Sat, 07 Sep 2024 11:51:35 GMT  
		Size: 791.3 KB (791278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68050e346d9f3d1ca1b5def57867ff17494b04f622c7c2c1bdec4df097c3834`  
		Last Modified: Sat, 07 Sep 2024 11:51:35 GMT  
		Size: 12.0 KB (12040 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; riscv64

```console
$ docker pull traefik@sha256:55d314e80da8fbb2c5173b6a760c940b41d806963614bcb6bae6f8559d3255dd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46636568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687199be3a20a6b32ada7e5ae6e105608c13d96563ab267b437abd45e30cda7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 09:08:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 07 Sep 2024 09:09:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 07 Sep 2024 09:09:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 07 Sep 2024 09:09:12 GMT
EXPOSE 80
# Sat, 07 Sep 2024 09:09:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 07 Sep 2024 09:09:13 GMT
CMD ["traefik"]
# Sat, 07 Sep 2024 09:09:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6191848a26e3a4e239baa081e92b80fed8492c8da548ad1be1f1ddba62cf4e1a`  
		Last Modified: Sat, 07 Sep 2024 09:10:14 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51249d46190dd7303b797d190f8a4abca1006265ccfdced07558a0cb85fc93d5`  
		Last Modified: Sat, 07 Sep 2024 09:10:56 GMT  
		Size: 42.8 MB (42808966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785056ce04e2c9bd1db5fd7aa106a1a04be0e2b08725ef2f719788bc930e54d5`  
		Last Modified: Sat, 07 Sep 2024 09:10:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:comte` - linux; s390x

```console
$ docker pull traefik@sha256:f6877172487f428997a7b0fa0c8bcbc64ac41270b0d53f722fb358dab04018ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46914466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e9cd18cde567de607fdfab463c4d9540b4fad818f98b8089938c4de70ec0b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 06 Aug 2024 14:12:12 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 14:12:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 14:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 14:12:12 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 14:12:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f7e4f1a84977bf705e64fc27016d89cd6be6039eac2042eae0f410b9bea208`  
		Last Modified: Sat, 07 Sep 2024 10:57:49 GMT  
		Size: 456.1 KB (456125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2428ea4c20b26697d969eb71827d50a3a142d5e6efbfefc05780a908b7642aa`  
		Last Modified: Sat, 07 Sep 2024 10:57:49 GMT  
		Size: 43.0 MB (42996374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c63f2ddefefb5440d84742626e3db7a7e0abae76b7b1b57238072a35a7829fb`  
		Last Modified: Sat, 07 Sep 2024 10:57:48 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:59c76a3905f4b9cffebe50fc6e4c289b50a46f48739d74d1b875bf550b7d4e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **803.2 KB (803220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838858b924ddd5172f42d65778e68c19a75bc53fcd3ac2595e23a196798bc925`

```dockerfile
```

-	Layers:
	-	`sha256:28f87c3a8e0e5bcfa1d1164c0a1640ecefb1078e7375557880698939f88cb85d`  
		Last Modified: Sat, 07 Sep 2024 10:57:48 GMT  
		Size: 791.2 KB (791232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562e149897b4b3022f1b79102c5f736cff9a9b112e8af6ede84d769a18b6da3b`  
		Last Modified: Sat, 07 Sep 2024 10:57:48 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json
