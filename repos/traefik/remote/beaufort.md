## `traefik:beaufort`

```console
$ docker pull traefik@sha256:9fc1c94d089d090891836139d25f7d47a7e38482b688accd4f007cc44769382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:28d8480aaac217f4ad85bbce5cd5fa516095b49a50c249aa874939a909453bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45170288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0903c18f51988c8ea9c569113b06a5cd709bdbae2654ad8ba2073bf77aa02395`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:52:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:52:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:52:14 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:52:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:52:14 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44ecee72e822b5008b09918187fdd2017803e9c45293cd4e957e6a57c3814`  
		Last Modified: Sat, 27 Jan 2024 03:56:50 GMT  
		Size: 622.2 KB (622159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c750850703a544234c94a1061ceae1c063a842406e4c991d7fd5c847ef079603`  
		Last Modified: Wed, 13 Mar 2024 19:52:35 GMT  
		Size: 41.1 MB (41139032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e9b1301485f057bf7fc6a6b90f50fdf0eda46734049e6e719ff32696c871fd`  
		Last Modified: Wed, 13 Mar 2024 19:52:28 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c48bcc4b9e1dc4a89e39fd8501d41a0d8fc0141c72921efc425f8b617078c79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42392870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c0c6225ebd15d2bff241fb30427ce058757ca8ddd2a87d1283bec4e957ed95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 14 Mar 2024 01:11:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 14 Mar 2024 01:11:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 14 Mar 2024 01:11:37 GMT
EXPOSE 80
# Thu, 14 Mar 2024 01:11:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 01:11:37 GMT
CMD ["traefik"]
# Thu, 14 Mar 2024 01:11:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e025885c4ea1368dd04ecf92b0cc3d3629cbcc04b3ce166fd86dfc1c18dc8`  
		Last Modified: Sat, 27 Jan 2024 09:31:21 GMT  
		Size: 623.4 KB (623387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce556492655026f150d858044f728b22d2cc2e8387f7f173c3d54e38176aa65b`  
		Last Modified: Thu, 14 Mar 2024 01:11:56 GMT  
		Size: 38.6 MB (38603719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41755d88f47c304a126cb216fb9a86385708d81eb251eec681b304bda37b5d8c`  
		Last Modified: Thu, 14 Mar 2024 01:11:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e68604ff497f79d9522e437ee66a3645de33494a2767872371a803212039993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42043483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1f8efc9eb622c56f587602b707c3238b25d6f32d32d008b9a33cd7ac516216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:32 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:32 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e9487662ce49d04a55c69f1640870789f94bfd6e0dc32a28c511ddd3489b71`  
		Last Modified: Sat, 16 Mar 2024 02:43:55 GMT  
		Size: 38.1 MB (38072646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c15ff70d10a381654357ae74e33269071ee5380f03f4e11119fb2c8b79fb51d`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:5df2a7a48bbc7bc8b9102d1be19ed7739db46a811c7c17632a4e0e1556913d31
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f4c4e50756136ce84a3d6ce131ef01d217d7d9841d00f1667291dbe06c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:26:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:26:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:26:53 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:26:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:26:54 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:26:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84276c557c55d0b763d852100a27cf507630a42743be661153455e374884705`  
		Last Modified: Wed, 13 Mar 2024 19:27:19 GMT  
		Size: 36.9 MB (36929877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd405b5f66d9a4da08abf8b723fadb8e19e062ca8f136c78b09f51d12abd0f`  
		Last Modified: Wed, 13 Mar 2024 19:27:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:b08d1fc83e10b985fec28bb86bba3038695d79cf623a1608b5ebe0a1ed88f17a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229524bf9d634c12b6ca11f397249459cf0c6b6b73d599d45f8b237e7001854`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 20:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 20:29:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 20:29:12 GMT
EXPOSE 80
# Wed, 13 Mar 2024 20:29:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 20:29:13 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 20:29:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947c294ec78d988aafdda154262ed90cfca050140faae69fb157fda0afe46e8`  
		Last Modified: Wed, 13 Mar 2024 20:32:14 GMT  
		Size: 39.9 MB (39933272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a82447626ce9aea1a2e5c7e6129e91ba0bf38d7f24139e53f5fb363c3b26f`  
		Last Modified: Wed, 13 Mar 2024 20:32:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
