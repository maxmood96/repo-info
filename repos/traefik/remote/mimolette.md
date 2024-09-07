## `traefik:mimolette`

```console
$ docker pull traefik@sha256:3d81ed54a9b7351729fe26a169f94dd0ba9d822e29444956dde9ec620e0065b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:ae7e8d7abb74d6b26bac80a24eb837e00ea9d9c9532455c6cf20ec66a6c112f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46902959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0812f2f47d1ce2e266281ec306160d1e322a063d3fd801fbffa46e669af7bf15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:55:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 07 Sep 2024 02:55:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 07 Sep 2024 02:55:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 07 Sep 2024 02:55:35 GMT
EXPOSE 80
# Sat, 07 Sep 2024 02:55:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 07 Sep 2024 02:55:36 GMT
CMD ["traefik"]
# Sat, 07 Sep 2024 02:55:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fb492bae2a7b261805e87e8aed80dd8c6e2a3baf3489a289e3a76fc9b1583b`  
		Last Modified: Sat, 07 Sep 2024 02:55:46 GMT  
		Size: 455.0 KB (454960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196250ba770d39f1ad16ea8b5505e5530efc865f4ecc94edb5c8c1ce6d398f3`  
		Last Modified: Sat, 07 Sep 2024 02:56:14 GMT  
		Size: 42.8 MB (42823824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a4eb37e552444bf8fd2da13fa62267fa2e077f7be1358aac9073b507a10a5e`  
		Last Modified: Sat, 07 Sep 2024 02:56:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef1115cecee068499d8311fdb45aa57ac64604d64cb753454329943c1ceb39db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44097658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c884ee3ae80a58fef5defc653842bf23a8128b9932f19aa4ae0724177fd7ad1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 13:26:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 13:26:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 13:26:39 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 13:26:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 13:26:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 13:26:39 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 13:26:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e79c95fa88637fb24f8efe3882fdafbfcd1a9997b2aa3bf1efc134c1eb64b`  
		Last Modified: Fri, 06 Sep 2024 21:20:55 GMT  
		Size: 456.0 KB (456010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229669de249cbeae308b5596305c9059f324b9283273881f721ae69d7ab6703d`  
		Last Modified: Fri, 06 Sep 2024 21:21:25 GMT  
		Size: 40.3 MB (40276090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272bb9fef300d218817b48354020e9cbfca88c38de0927a7d4cbfcaae96d92e6`  
		Last Modified: Fri, 06 Sep 2024 21:21:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:0c620102ab6ec2ac37847426eb1ae2ff42d59f783cd3e7dc7a2c9dd7fc18f4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 KB (11582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b31f30ab280b5443108e8bf6e46a35dffb7f80e64689cffee58c674e60209c`

```dockerfile
```

-	Layers:
	-	`sha256:a5882ef74ffbc25f96f609db79a8b3566a0346df77d3f4f4c6bead59b34b372b`  
		Last Modified: Fri, 06 Sep 2024 21:21:23 GMT  
		Size: 11.6 KB (11582 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b0d6e1146f495e897daf848afe4b7d4baaa58c40cfe4613f9e28c6d1961c3b9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44234712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c7e9763d52ea2d836ff14ad3f602ef9b403ca49f975c0f25e978b611e35078`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:47:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 06 Aug 2024 19:41:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 06 Aug 2024 19:41:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 06 Aug 2024 19:41:05 GMT
EXPOSE 80
# Tue, 06 Aug 2024 19:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 19:41:06 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 19:41:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53df005727c4531718692629248a4acf9fcca84ebd56edab34cfb7439e3157c2`  
		Last Modified: Tue, 23 Jul 2024 02:47:56 GMT  
		Size: 463.7 KB (463747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f367371ee58e07e9568f0fd6a7334361f887cc4aef9a8332a4f25b1e3cd75f4`  
		Last Modified: Tue, 06 Aug 2024 19:41:41 GMT  
		Size: 39.7 MB (39683663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec514ea593973e90dd2e7963b038aa214876241fe3c671b71e447c5748fddd30`  
		Last Modified: Tue, 06 Aug 2024 19:41:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:34a09e4dea74e4d1e7ef34d8e109ff88ce8d22cac67d292a58f5dd136e4efdf6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42576339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e26565596f580d8b55c617e78400442ae72f8011b471f07abf0933844ad762d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:08:18 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 07 Sep 2024 02:08:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 07 Sep 2024 02:08:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 07 Sep 2024 02:08:42 GMT
EXPOSE 80
# Sat, 07 Sep 2024 02:08:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 07 Sep 2024 02:08:43 GMT
CMD ["traefik"]
# Sat, 07 Sep 2024 02:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3c15b75f2da1c800c7cc70e87f691399e6bd97173886ce657397ec27a6ea29`  
		Last Modified: Sat, 07 Sep 2024 02:08:56 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc52d42b0cd1b0caae8d48104eef590f662113d7d8a404068dd26173e3177c6`  
		Last Modified: Sat, 07 Sep 2024 02:09:23 GMT  
		Size: 38.5 MB (38545806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c0a81a912dc8b2512cbdb3e019b93771f167c105146ac6cdaa458ecb7175b5`  
		Last Modified: Sat, 07 Sep 2024 02:09:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:b0141090d672afa27d1e542b422cc9e7f1d42db0571004f4334190414438fad0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45318413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386c7e2c1c264adc2194163d89cac2fc024759a3fc8b3a92e9bead6b01214914`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 12:44:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 06 Aug 2024 20:10:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 06 Aug 2024 20:10:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 06 Aug 2024 20:10:10 GMT
EXPOSE 80
# Tue, 06 Aug 2024 20:10:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 20:10:11 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 20:10:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3220e9e4f206b6ef30443855a7d18341eb7e8a6c5825f79355c757a1f65b3d`  
		Last Modified: Tue, 23 Jul 2024 12:48:05 GMT  
		Size: 462.4 KB (462409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7ffae4aa689462848c5e24e39c998de6fb1a5487db354bf3c52367115d3017`  
		Last Modified: Tue, 06 Aug 2024 20:12:13 GMT  
		Size: 41.5 MB (41484963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5ad0008a3d37aff608189b824ea1abe4d140bdccc3164e4a9ba58f7564323`  
		Last Modified: Tue, 06 Aug 2024 20:11:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:02668579c45a133546fc31709b56fbacfd912464616ce96a6cf8859528a53c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45649276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04682764f4d714ad808a5d034498d7e721a694949fa2a2730a68c4a107f2c7b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 13:26:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 06 Aug 2024 13:26:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 06 Aug 2024 13:26:39 GMT
COPY entrypoint.sh / # buildkit
# Tue, 06 Aug 2024 13:26:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 06 Aug 2024 13:26:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 13:26:39 GMT
CMD ["traefik"]
# Tue, 06 Aug 2024 13:26:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1d866f6644ffb48d37d26017fea91ad2d7ad4d93f892a43323b5ad0fa0159`  
		Last Modified: Fri, 06 Sep 2024 21:08:52 GMT  
		Size: 456.1 KB (456109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9dd3b60774653604b82fa0217cd671e688c3190d16ff8e47566f5851f9b70`  
		Last Modified: Fri, 06 Sep 2024 21:09:54 GMT  
		Size: 41.7 MB (41731734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19e05dc059948c18fc0c54a11c0221391ab8ce5d04d1c383d391a2dc7feb47`  
		Last Modified: Fri, 06 Sep 2024 21:09:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:0a8ee139181f7ac4df005091f4fd502de60f2c1c7ad70919b60018d82ce3e13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **803.6 KB (803552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1631bc5b28a5e170acc171999f1fa31039f7b6150199115915ee34016e754419`

```dockerfile
```

-	Layers:
	-	`sha256:ae1569a699992d7237d263afe7605d3ea67d24efc3c0d00739783412b8c5db9b`  
		Last Modified: Fri, 06 Sep 2024 21:09:53 GMT  
		Size: 791.8 KB (791839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d5b67b0eff1ffdf9c47b95ded5caca85bb4f940c06df3adb1dae11520e5d24`  
		Last Modified: Fri, 06 Sep 2024 21:09:53 GMT  
		Size: 11.7 KB (11713 bytes)  
		MIME: application/vnd.in-toto+json
