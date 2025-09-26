## `traefik:latest`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json
