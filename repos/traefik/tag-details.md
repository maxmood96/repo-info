<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.29`](#traefik21129)
-	[`traefik:2.11.29-nanoserver-ltsc2022`](#traefik21129-nanoserver-ltsc2022)
-	[`traefik:2.11.29-windowsservercore-ltsc2022`](#traefik21129-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.5`](#traefik35)
-	[`traefik:3.5-nanoserver-ltsc2022`](#traefik35-nanoserver-ltsc2022)
-	[`traefik:3.5-windowsservercore-ltsc2022`](#traefik35-windowsservercore-ltsc2022)
-	[`traefik:3.5.1`](#traefik351)
-	[`traefik:3.5.1-nanoserver-ltsc2022`](#traefik351-nanoserver-ltsc2022)
-	[`traefik:3.5.1-windowsservercore-ltsc2022`](#traefik351-windowsservercore-ltsc2022)
-	[`traefik:chabichou`](#traefikchabichou)
-	[`traefik:chabichou-nanoserver-ltsc2022`](#traefikchabichou-nanoserver-ltsc2022)
-	[`traefik:chabichou-windowsservercore-ltsc2022`](#traefikchabichou-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.29`](#traefikv21129)
-	[`traefik:v2.11.29-nanoserver-ltsc2022`](#traefikv21129-nanoserver-ltsc2022)
-	[`traefik:v2.11.29-windowsservercore-ltsc2022`](#traefikv21129-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.5`](#traefikv35)
-	[`traefik:v3.5-nanoserver-ltsc2022`](#traefikv35-nanoserver-ltsc2022)
-	[`traefik:v3.5-windowsservercore-ltsc2022`](#traefikv35-windowsservercore-ltsc2022)
-	[`traefik:v3.5.1`](#traefikv351)
-	[`traefik:v3.5.1-nanoserver-ltsc2022`](#traefikv351-nanoserver-ltsc2022)
-	[`traefik:v3.5.1-windowsservercore-ltsc2022`](#traefikv351-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:247c456388728396fda0cb8e500c0d5d83d0624cc364623479cca4cb0fa5257c
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
$ docker pull traefik@sha256:eace18564ef3561b118e8ff545ad8a797d58361120b6d9c2dbbceae0cf346e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57309580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f17a37e9ce42281a054291bc15ecd02405d77302804568ee294c95e5385a6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6a5cdd866efd861489b415dda275d6ce32b233e7eb29b2a9259c65bb5db14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 447.7 KB (447748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac00a37161f2cd17d2443066bbe78745e414c1f89c06a17b8992c1cec3efef9`  
		Last Modified: Wed, 23 Jul 2025 16:33:34 GMT  
		Size: 53.1 MB (53061775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb59abe3b0a1ff06fea7cefb2275bb69f4fa1c26ba5a2ecddfbca1380f2b14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:9aa380b54283255b56637bf35c48c2f6a21caa8ee8ef7c358481e912ecce5e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.4 KB (849431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3debe7e46ccc175361251232da545bb603cfc2e0c6b4d655593d172327b52ba6`

```dockerfile
```

-	Layers:
	-	`sha256:5d0369d1eeb2023fa9f21c7c7fd2e83d56d881638535a956a289269188fa2150`  
		Last Modified: Wed, 23 Jul 2025 18:09:31 GMT  
		Size: 836.9 KB (836893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d7f53175c2f28073e37ece4d4dc48e130e63712c3bd5e132bba61b8b6b9685`  
		Last Modified: Wed, 23 Jul 2025 18:09:32 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3b059ca4a87278ff181ed806fbf657026e327109d6079d80a8c0c4c0cdacbdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52818665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9cebe2fdfc292987e3ce352ac2023eee313a637f075dca309bddd8a00af07e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfa5cb7a6623eef4b1b94d54b62dac25a94d091779e9bf28af0cf01c45ca2d`  
		Last Modified: Wed, 23 Jul 2025 16:34:10 GMT  
		Size: 48.9 MB (48869104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d885957a48ebf1a8a1e1991c221e0db29e865eb0504cab9b026d1a11e36ab8`  
		Last Modified: Wed, 23 Jul 2025 16:33:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:8da48b1c582aa61129a65d0f2ac8be3ea8c2673a181ca7260a48ac74584b94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38327b809aa8068bc122115eaae98758ba03e2b538e26aca37363b1753bd4ff`

```dockerfile
```

-	Layers:
	-	`sha256:0c1d01b03dd1458bb84010574efda803684f13e85a08eabd8e249e4418375bd4`  
		Last Modified: Wed, 23 Jul 2025 18:09:36 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6ddbad673d635cfcc5310a40c5dadc078a4b64d90556a5ab9e197ffe7dcf6859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53266740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd18da0fa25cebbaa78e08beca3e8070d7d69d54e601f00ccdf42a29e375475`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58277fe9b3169f6c6e833dc3c076e6d8cb8174013cfe6f675afb94a7f7caab05`  
		Last Modified: Wed, 23 Jul 2025 19:31:17 GMT  
		Size: 48.7 MB (48686068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9f979bbc32d71453cbbe2751427e6dfbfc3c2a281b309abd387fe1606e76b`  
		Last Modified: Wed, 23 Jul 2025 19:30:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:23e6e27b147c936ad1a393824ae8dbc59e48e0a43bdf97569666573c67f3e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.7 KB (849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b388664c8958e931f7340b10a4dcf06dda25cb8728e640743d20ec8ad1b21702`

```dockerfile
```

-	Layers:
	-	`sha256:330bcf63716e07b7186b61355799a0cf06b0f303b194d36a62225dfa37263e0f`  
		Last Modified: Wed, 23 Jul 2025 21:09:25 GMT  
		Size: 837.0 KB (836985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c89d5d71fbd80b601818f304f19d8982e45ee54bf0459f7f3bcfe9d3e6aa060`  
		Last Modified: Wed, 23 Jul 2025 21:09:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:a81a44141f7213e1b092174f1973aa4fd5f4c3378ea86aa42c0aef77d9a7f5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50979077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de43156b6777f5b6f72104badcdd333f2fa121df66e138057fb8be91d224ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e7a31a18f6e6e899e667847ce220f7725234d795b03928bf3211e58095136`  
		Last Modified: Wed, 23 Jul 2025 16:37:05 GMT  
		Size: 46.8 MB (46801622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02516bbfead5cba4f2b832f27c41cc0df4ce6bb074634717a160f6967fa760b9`  
		Last Modified: Wed, 23 Jul 2025 16:36:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c3484201ee4e7182e642b40d6bcb57af8cf9308c8a6fa008c0ae60600438bdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84a36a92126d60b210234018655172988e3c8ea27eb8475bb27a3e02d6e0a73`

```dockerfile
```

-	Layers:
	-	`sha256:196ee66fd2f4875fabda3d528b89003582ae4086daf819b4dfe7955b5d75b162`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 835.0 KB (834994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c108b88851183a022b367338f8ace2870f73cec93bf01f3b14034663cc5b7cf7`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:2e85387c795128f7ff75629d7e35cbe7206d2eac04fe8e3a8e74b09f3b5d4e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55737852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53367cfc6dacbafdef52b7cefff9e0a369d896ea358dd26cbcd097eb57c0795a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413b15af1ed5672dd303a347ef10c877277d4f19ac5ff5176eef18b3c92e04`  
		Last Modified: Wed, 23 Jul 2025 16:37:35 GMT  
		Size: 51.6 MB (51643924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e671768c8963282ff7f9960c8c83f7bf31991bfb534c47038b1f44a519c85`  
		Last Modified: Wed, 23 Jul 2025 16:37:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a22d26f7c4e43335665bc36fca121703bdc16b4cb6bf30210d2155990694321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.5 KB (847476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a63c056bb163e95afc87cb51fe62add83421a277021e0c2dfa95515f80b76`

```dockerfile
```

-	Layers:
	-	`sha256:63ce6d68b037cf9e8c6fd69e195dc051128a3197dbdf2bfb7d420b6ec107745b`  
		Last Modified: Wed, 23 Jul 2025 18:09:53 GMT  
		Size: 834.9 KB (834938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c7146e9bff055a3bded60dde2df0a298a2c44e101257ac1fa08e684c152124`  
		Last Modified: Wed, 23 Jul 2025 18:09:54 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e07baca183e30daec3cdcbc889b097f6f54f4c40f48e0e8b0bf9c6872097e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:8783408c30c7d87a133c97b470eee4b6cb6072904d86ed3bcb0a01b86d57e555
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176887853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b9a266f3a23e0db5f2ce2129d8912a932c67b56cfc9473f702b84e4fbc5ce8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:54:21 GMT
RUN cmd /S /C #(nop) COPY file:3620d5ee3c62a9a7defdfe776efbe134e9eec74e652602e8b680a1191d27cabb in \ 
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:54:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6fa0a5e9c270703af7127826f05971b64e43231e48d8e574f15cab8ef0a09`  
		Last Modified: Tue, 12 Aug 2025 20:55:08 GMT  
		Size: 54.2 MB (54224431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212aebf7ca03b11173fe9d2aeff59f530551fcad130514a7e334c2a3bb884328`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53582a3f4bca191593751e24893d8762fc600a76af2e2797b4b706521522911d`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42da9828e2256a0f08dfc92a2f4127462721ca8932bda3373440095775d1cfb2`  
		Last Modified: Tue, 12 Aug 2025 20:54:59 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:853eb314cf37dc5bead571fd52e07c7271a611cbd1bec848e19fec77d55cda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:875060b1d629ff2fa7a0a9c8a9c712120b573dacf292fc7da1486bf284f74cfc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b0bf9585615a88c24c687d45ade21e5b77835415315e38c70d96e57558526`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:27:16 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:27:17 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:27:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f347076885ded40c10d46a46c8a41531675af1341717251d8d2cf2cc56897867`  
		Last Modified: Tue, 12 Aug 2025 20:28:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafab50289b5b2a42095e99f8e95ccb9ac8364895d938a41a4bb5c03c279173e`  
		Last Modified: Tue, 12 Aug 2025 20:29:16 GMT  
		Size: 54.7 MB (54697384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906cfb424debae93facac029ac7273d434af16a0c5720febb8e1137fad67edb4`  
		Last Modified: Tue, 12 Aug 2025 20:28:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff90e4a3c7aeefd845bea3efc05ab9cdae6e23b13f39b2d934cc116f56f126c0`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1acd00a8475b3da17632d0438701092087f9ada69be46bd7031a59c584a79`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:247c456388728396fda0cb8e500c0d5d83d0624cc364623479cca4cb0fa5257c
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
$ docker pull traefik@sha256:eace18564ef3561b118e8ff545ad8a797d58361120b6d9c2dbbceae0cf346e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57309580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f17a37e9ce42281a054291bc15ecd02405d77302804568ee294c95e5385a6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6a5cdd866efd861489b415dda275d6ce32b233e7eb29b2a9259c65bb5db14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 447.7 KB (447748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac00a37161f2cd17d2443066bbe78745e414c1f89c06a17b8992c1cec3efef9`  
		Last Modified: Wed, 23 Jul 2025 16:33:34 GMT  
		Size: 53.1 MB (53061775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb59abe3b0a1ff06fea7cefb2275bb69f4fa1c26ba5a2ecddfbca1380f2b14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9aa380b54283255b56637bf35c48c2f6a21caa8ee8ef7c358481e912ecce5e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.4 KB (849431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3debe7e46ccc175361251232da545bb603cfc2e0c6b4d655593d172327b52ba6`

```dockerfile
```

-	Layers:
	-	`sha256:5d0369d1eeb2023fa9f21c7c7fd2e83d56d881638535a956a289269188fa2150`  
		Last Modified: Wed, 23 Jul 2025 18:09:31 GMT  
		Size: 836.9 KB (836893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d7f53175c2f28073e37ece4d4dc48e130e63712c3bd5e132bba61b8b6b9685`  
		Last Modified: Wed, 23 Jul 2025 18:09:32 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3b059ca4a87278ff181ed806fbf657026e327109d6079d80a8c0c4c0cdacbdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52818665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9cebe2fdfc292987e3ce352ac2023eee313a637f075dca309bddd8a00af07e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfa5cb7a6623eef4b1b94d54b62dac25a94d091779e9bf28af0cf01c45ca2d`  
		Last Modified: Wed, 23 Jul 2025 16:34:10 GMT  
		Size: 48.9 MB (48869104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d885957a48ebf1a8a1e1991c221e0db29e865eb0504cab9b026d1a11e36ab8`  
		Last Modified: Wed, 23 Jul 2025 16:33:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:8da48b1c582aa61129a65d0f2ac8be3ea8c2673a181ca7260a48ac74584b94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38327b809aa8068bc122115eaae98758ba03e2b538e26aca37363b1753bd4ff`

```dockerfile
```

-	Layers:
	-	`sha256:0c1d01b03dd1458bb84010574efda803684f13e85a08eabd8e249e4418375bd4`  
		Last Modified: Wed, 23 Jul 2025 18:09:36 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6ddbad673d635cfcc5310a40c5dadc078a4b64d90556a5ab9e197ffe7dcf6859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53266740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd18da0fa25cebbaa78e08beca3e8070d7d69d54e601f00ccdf42a29e375475`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58277fe9b3169f6c6e833dc3c076e6d8cb8174013cfe6f675afb94a7f7caab05`  
		Last Modified: Wed, 23 Jul 2025 19:31:17 GMT  
		Size: 48.7 MB (48686068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9f979bbc32d71453cbbe2751427e6dfbfc3c2a281b309abd387fe1606e76b`  
		Last Modified: Wed, 23 Jul 2025 19:30:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:23e6e27b147c936ad1a393824ae8dbc59e48e0a43bdf97569666573c67f3e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.7 KB (849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b388664c8958e931f7340b10a4dcf06dda25cb8728e640743d20ec8ad1b21702`

```dockerfile
```

-	Layers:
	-	`sha256:330bcf63716e07b7186b61355799a0cf06b0f303b194d36a62225dfa37263e0f`  
		Last Modified: Wed, 23 Jul 2025 21:09:25 GMT  
		Size: 837.0 KB (836985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c89d5d71fbd80b601818f304f19d8982e45ee54bf0459f7f3bcfe9d3e6aa060`  
		Last Modified: Wed, 23 Jul 2025 21:09:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:a81a44141f7213e1b092174f1973aa4fd5f4c3378ea86aa42c0aef77d9a7f5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50979077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de43156b6777f5b6f72104badcdd333f2fa121df66e138057fb8be91d224ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e7a31a18f6e6e899e667847ce220f7725234d795b03928bf3211e58095136`  
		Last Modified: Wed, 23 Jul 2025 16:37:05 GMT  
		Size: 46.8 MB (46801622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02516bbfead5cba4f2b832f27c41cc0df4ce6bb074634717a160f6967fa760b9`  
		Last Modified: Wed, 23 Jul 2025 16:36:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c3484201ee4e7182e642b40d6bcb57af8cf9308c8a6fa008c0ae60600438bdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84a36a92126d60b210234018655172988e3c8ea27eb8475bb27a3e02d6e0a73`

```dockerfile
```

-	Layers:
	-	`sha256:196ee66fd2f4875fabda3d528b89003582ae4086daf819b4dfe7955b5d75b162`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 835.0 KB (834994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c108b88851183a022b367338f8ace2870f73cec93bf01f3b14034663cc5b7cf7`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:2e85387c795128f7ff75629d7e35cbe7206d2eac04fe8e3a8e74b09f3b5d4e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55737852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53367cfc6dacbafdef52b7cefff9e0a369d896ea358dd26cbcd097eb57c0795a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413b15af1ed5672dd303a347ef10c877277d4f19ac5ff5176eef18b3c92e04`  
		Last Modified: Wed, 23 Jul 2025 16:37:35 GMT  
		Size: 51.6 MB (51643924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e671768c8963282ff7f9960c8c83f7bf31991bfb534c47038b1f44a519c85`  
		Last Modified: Wed, 23 Jul 2025 16:37:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a22d26f7c4e43335665bc36fca121703bdc16b4cb6bf30210d2155990694321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.5 KB (847476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a63c056bb163e95afc87cb51fe62add83421a277021e0c2dfa95515f80b76`

```dockerfile
```

-	Layers:
	-	`sha256:63ce6d68b037cf9e8c6fd69e195dc051128a3197dbdf2bfb7d420b6ec107745b`  
		Last Modified: Wed, 23 Jul 2025 18:09:53 GMT  
		Size: 834.9 KB (834938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c7146e9bff055a3bded60dde2df0a298a2c44e101257ac1fa08e684c152124`  
		Last Modified: Wed, 23 Jul 2025 18:09:54 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e07baca183e30daec3cdcbc889b097f6f54f4c40f48e0e8b0bf9c6872097e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:8783408c30c7d87a133c97b470eee4b6cb6072904d86ed3bcb0a01b86d57e555
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176887853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b9a266f3a23e0db5f2ce2129d8912a932c67b56cfc9473f702b84e4fbc5ce8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:54:21 GMT
RUN cmd /S /C #(nop) COPY file:3620d5ee3c62a9a7defdfe776efbe134e9eec74e652602e8b680a1191d27cabb in \ 
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:54:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6fa0a5e9c270703af7127826f05971b64e43231e48d8e574f15cab8ef0a09`  
		Last Modified: Tue, 12 Aug 2025 20:55:08 GMT  
		Size: 54.2 MB (54224431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212aebf7ca03b11173fe9d2aeff59f530551fcad130514a7e334c2a3bb884328`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53582a3f4bca191593751e24893d8762fc600a76af2e2797b4b706521522911d`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42da9828e2256a0f08dfc92a2f4127462721ca8932bda3373440095775d1cfb2`  
		Last Modified: Tue, 12 Aug 2025 20:54:59 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:853eb314cf37dc5bead571fd52e07c7271a611cbd1bec848e19fec77d55cda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:875060b1d629ff2fa7a0a9c8a9c712120b573dacf292fc7da1486bf284f74cfc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b0bf9585615a88c24c687d45ade21e5b77835415315e38c70d96e57558526`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:27:16 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:27:17 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:27:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f347076885ded40c10d46a46c8a41531675af1341717251d8d2cf2cc56897867`  
		Last Modified: Tue, 12 Aug 2025 20:28:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafab50289b5b2a42095e99f8e95ccb9ac8364895d938a41a4bb5c03c279173e`  
		Last Modified: Tue, 12 Aug 2025 20:29:16 GMT  
		Size: 54.7 MB (54697384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906cfb424debae93facac029ac7273d434af16a0c5720febb8e1137fad67edb4`  
		Last Modified: Tue, 12 Aug 2025 20:28:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff90e4a3c7aeefd845bea3efc05ab9cdae6e23b13f39b2d934cc116f56f126c0`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1acd00a8475b3da17632d0438701092087f9ada69be46bd7031a59c584a79`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29`

**does not exist** (yet?)

## `traefik:2.11.29-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:2.11.29-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:3`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:baa1b677ba2fcbdd9b8a16468ac8658fa34eda0045eb2ca2ee96d0cd8965ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:b850b454cd1c1c6d01665d5439a7d5725f03adccdc7ce6d2301a217af76c5a0a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406bc0a7ea074b91bd504e4ec165c902b9b8da8f58476453c9ca9204f113ecb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:53:04 GMT
RUN cmd /S /C #(nop) COPY file:e7f35439209ec29fad086d717d9f4b58df9184ed229cdee84cb5c209ee80d802 in \ 
# Tue, 12 Aug 2025 20:53:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:53:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:53:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01614d8c42e78a58dcef6b52233a7b481a0541922c151631983a3fd0b16e4e7`  
		Last Modified: Tue, 12 Aug 2025 20:53:56 GMT  
		Size: 55.2 MB (55179587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696fa452e8de21ab6cc0d0c918542ee1831e6d1250ed84f00e993f099957c06a`  
		Last Modified: Tue, 12 Aug 2025 20:53:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d093d691eb644f9d3e3c1867f5245e592f16f8df58f7767cd9f1d1f59ff54b4`  
		Last Modified: Tue, 12 Aug 2025 20:53:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720cd3751519320b63bb908878b5b2ad7692ca12c748a962665956ba668ecf3`  
		Last Modified: Tue, 12 Aug 2025 20:53:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:70dae286d3ae856e84305cc7cc1cdd0cbc73d1fd4158845701e6b868ba9e64ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:9971225eda327cebfe6f76283cbee8c64aa29fe78fce7308d28fdf7706c6e818
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75016ca88cd12f5dfa7cb23e18005619b06aa7dec182d13d5b771ef84bed6093`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:28:50 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:28:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9246f832a03d0625295a77b39c6a9f51241182680e05091f53edcd2648a555`  
		Last Modified: Tue, 12 Aug 2025 20:30:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e24f5510416f611ed431d176a07703b8b7cecd5b1afeccb472572f9bd1992d`  
		Last Modified: Tue, 12 Aug 2025 20:30:53 GMT  
		Size: 55.7 MB (55671777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926afb979507dd2cf7ed44703c7160f4c267c76a1e39900efeb6dc3f6e9fa2f`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a29f819c57f55f3c31c6f7d038136bdfbc9fe14f89138541b80c78a4591bdc`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7532a193c37cf8f3b9742e116a8ba96c5e2f73f11f9afe5b382aed9c603ee02`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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

### `traefik:3.5` - linux; amd64

```console
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:baa1b677ba2fcbdd9b8a16468ac8658fa34eda0045eb2ca2ee96d0cd8965ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:b850b454cd1c1c6d01665d5439a7d5725f03adccdc7ce6d2301a217af76c5a0a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406bc0a7ea074b91bd504e4ec165c902b9b8da8f58476453c9ca9204f113ecb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:53:04 GMT
RUN cmd /S /C #(nop) COPY file:e7f35439209ec29fad086d717d9f4b58df9184ed229cdee84cb5c209ee80d802 in \ 
# Tue, 12 Aug 2025 20:53:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:53:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:53:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01614d8c42e78a58dcef6b52233a7b481a0541922c151631983a3fd0b16e4e7`  
		Last Modified: Tue, 12 Aug 2025 20:53:56 GMT  
		Size: 55.2 MB (55179587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696fa452e8de21ab6cc0d0c918542ee1831e6d1250ed84f00e993f099957c06a`  
		Last Modified: Tue, 12 Aug 2025 20:53:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d093d691eb644f9d3e3c1867f5245e592f16f8df58f7767cd9f1d1f59ff54b4`  
		Last Modified: Tue, 12 Aug 2025 20:53:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720cd3751519320b63bb908878b5b2ad7692ca12c748a962665956ba668ecf3`  
		Last Modified: Tue, 12 Aug 2025 20:53:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:70dae286d3ae856e84305cc7cc1cdd0cbc73d1fd4158845701e6b868ba9e64ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:9971225eda327cebfe6f76283cbee8c64aa29fe78fce7308d28fdf7706c6e818
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75016ca88cd12f5dfa7cb23e18005619b06aa7dec182d13d5b771ef84bed6093`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:28:50 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:28:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9246f832a03d0625295a77b39c6a9f51241182680e05091f53edcd2648a555`  
		Last Modified: Tue, 12 Aug 2025 20:30:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e24f5510416f611ed431d176a07703b8b7cecd5b1afeccb472572f9bd1992d`  
		Last Modified: Tue, 12 Aug 2025 20:30:53 GMT  
		Size: 55.7 MB (55671777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926afb979507dd2cf7ed44703c7160f4c267c76a1e39900efeb6dc3f6e9fa2f`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a29f819c57f55f3c31c6f7d038136bdfbc9fe14f89138541b80c78a4591bdc`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7532a193c37cf8f3b9742e116a8ba96c5e2f73f11f9afe5b382aed9c603ee02`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.1`

**does not exist** (yet?)

## `traefik:3.5.1-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:3.5.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:chabichou`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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

### `traefik:chabichou` - linux; amd64

```console
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:chabichou-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:baa1b677ba2fcbdd9b8a16468ac8658fa34eda0045eb2ca2ee96d0cd8965ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:b850b454cd1c1c6d01665d5439a7d5725f03adccdc7ce6d2301a217af76c5a0a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406bc0a7ea074b91bd504e4ec165c902b9b8da8f58476453c9ca9204f113ecb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:53:04 GMT
RUN cmd /S /C #(nop) COPY file:e7f35439209ec29fad086d717d9f4b58df9184ed229cdee84cb5c209ee80d802 in \ 
# Tue, 12 Aug 2025 20:53:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:53:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:53:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01614d8c42e78a58dcef6b52233a7b481a0541922c151631983a3fd0b16e4e7`  
		Last Modified: Tue, 12 Aug 2025 20:53:56 GMT  
		Size: 55.2 MB (55179587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696fa452e8de21ab6cc0d0c918542ee1831e6d1250ed84f00e993f099957c06a`  
		Last Modified: Tue, 12 Aug 2025 20:53:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d093d691eb644f9d3e3c1867f5245e592f16f8df58f7767cd9f1d1f59ff54b4`  
		Last Modified: Tue, 12 Aug 2025 20:53:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720cd3751519320b63bb908878b5b2ad7692ca12c748a962665956ba668ecf3`  
		Last Modified: Tue, 12 Aug 2025 20:53:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:70dae286d3ae856e84305cc7cc1cdd0cbc73d1fd4158845701e6b868ba9e64ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:9971225eda327cebfe6f76283cbee8c64aa29fe78fce7308d28fdf7706c6e818
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75016ca88cd12f5dfa7cb23e18005619b06aa7dec182d13d5b771ef84bed6093`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:28:50 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:28:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9246f832a03d0625295a77b39c6a9f51241182680e05091f53edcd2648a555`  
		Last Modified: Tue, 12 Aug 2025 20:30:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e24f5510416f611ed431d176a07703b8b7cecd5b1afeccb472572f9bd1992d`  
		Last Modified: Tue, 12 Aug 2025 20:30:53 GMT  
		Size: 55.7 MB (55671777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926afb979507dd2cf7ed44703c7160f4c267c76a1e39900efeb6dc3f6e9fa2f`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a29f819c57f55f3c31c6f7d038136bdfbc9fe14f89138541b80c78a4591bdc`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7532a193c37cf8f3b9742e116a8ba96c5e2f73f11f9afe5b382aed9c603ee02`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:247c456388728396fda0cb8e500c0d5d83d0624cc364623479cca4cb0fa5257c
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
$ docker pull traefik@sha256:eace18564ef3561b118e8ff545ad8a797d58361120b6d9c2dbbceae0cf346e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57309580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f17a37e9ce42281a054291bc15ecd02405d77302804568ee294c95e5385a6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6a5cdd866efd861489b415dda275d6ce32b233e7eb29b2a9259c65bb5db14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 447.7 KB (447748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac00a37161f2cd17d2443066bbe78745e414c1f89c06a17b8992c1cec3efef9`  
		Last Modified: Wed, 23 Jul 2025 16:33:34 GMT  
		Size: 53.1 MB (53061775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb59abe3b0a1ff06fea7cefb2275bb69f4fa1c26ba5a2ecddfbca1380f2b14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:9aa380b54283255b56637bf35c48c2f6a21caa8ee8ef7c358481e912ecce5e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.4 KB (849431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3debe7e46ccc175361251232da545bb603cfc2e0c6b4d655593d172327b52ba6`

```dockerfile
```

-	Layers:
	-	`sha256:5d0369d1eeb2023fa9f21c7c7fd2e83d56d881638535a956a289269188fa2150`  
		Last Modified: Wed, 23 Jul 2025 18:09:31 GMT  
		Size: 836.9 KB (836893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d7f53175c2f28073e37ece4d4dc48e130e63712c3bd5e132bba61b8b6b9685`  
		Last Modified: Wed, 23 Jul 2025 18:09:32 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3b059ca4a87278ff181ed806fbf657026e327109d6079d80a8c0c4c0cdacbdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52818665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9cebe2fdfc292987e3ce352ac2023eee313a637f075dca309bddd8a00af07e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfa5cb7a6623eef4b1b94d54b62dac25a94d091779e9bf28af0cf01c45ca2d`  
		Last Modified: Wed, 23 Jul 2025 16:34:10 GMT  
		Size: 48.9 MB (48869104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d885957a48ebf1a8a1e1991c221e0db29e865eb0504cab9b026d1a11e36ab8`  
		Last Modified: Wed, 23 Jul 2025 16:33:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:8da48b1c582aa61129a65d0f2ac8be3ea8c2673a181ca7260a48ac74584b94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38327b809aa8068bc122115eaae98758ba03e2b538e26aca37363b1753bd4ff`

```dockerfile
```

-	Layers:
	-	`sha256:0c1d01b03dd1458bb84010574efda803684f13e85a08eabd8e249e4418375bd4`  
		Last Modified: Wed, 23 Jul 2025 18:09:36 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6ddbad673d635cfcc5310a40c5dadc078a4b64d90556a5ab9e197ffe7dcf6859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53266740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd18da0fa25cebbaa78e08beca3e8070d7d69d54e601f00ccdf42a29e375475`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58277fe9b3169f6c6e833dc3c076e6d8cb8174013cfe6f675afb94a7f7caab05`  
		Last Modified: Wed, 23 Jul 2025 19:31:17 GMT  
		Size: 48.7 MB (48686068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9f979bbc32d71453cbbe2751427e6dfbfc3c2a281b309abd387fe1606e76b`  
		Last Modified: Wed, 23 Jul 2025 19:30:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:23e6e27b147c936ad1a393824ae8dbc59e48e0a43bdf97569666573c67f3e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.7 KB (849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b388664c8958e931f7340b10a4dcf06dda25cb8728e640743d20ec8ad1b21702`

```dockerfile
```

-	Layers:
	-	`sha256:330bcf63716e07b7186b61355799a0cf06b0f303b194d36a62225dfa37263e0f`  
		Last Modified: Wed, 23 Jul 2025 21:09:25 GMT  
		Size: 837.0 KB (836985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c89d5d71fbd80b601818f304f19d8982e45ee54bf0459f7f3bcfe9d3e6aa060`  
		Last Modified: Wed, 23 Jul 2025 21:09:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:a81a44141f7213e1b092174f1973aa4fd5f4c3378ea86aa42c0aef77d9a7f5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50979077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de43156b6777f5b6f72104badcdd333f2fa121df66e138057fb8be91d224ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e7a31a18f6e6e899e667847ce220f7725234d795b03928bf3211e58095136`  
		Last Modified: Wed, 23 Jul 2025 16:37:05 GMT  
		Size: 46.8 MB (46801622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02516bbfead5cba4f2b832f27c41cc0df4ce6bb074634717a160f6967fa760b9`  
		Last Modified: Wed, 23 Jul 2025 16:36:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c3484201ee4e7182e642b40d6bcb57af8cf9308c8a6fa008c0ae60600438bdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84a36a92126d60b210234018655172988e3c8ea27eb8475bb27a3e02d6e0a73`

```dockerfile
```

-	Layers:
	-	`sha256:196ee66fd2f4875fabda3d528b89003582ae4086daf819b4dfe7955b5d75b162`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 835.0 KB (834994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c108b88851183a022b367338f8ace2870f73cec93bf01f3b14034663cc5b7cf7`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:2e85387c795128f7ff75629d7e35cbe7206d2eac04fe8e3a8e74b09f3b5d4e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55737852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53367cfc6dacbafdef52b7cefff9e0a369d896ea358dd26cbcd097eb57c0795a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413b15af1ed5672dd303a347ef10c877277d4f19ac5ff5176eef18b3c92e04`  
		Last Modified: Wed, 23 Jul 2025 16:37:35 GMT  
		Size: 51.6 MB (51643924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e671768c8963282ff7f9960c8c83f7bf31991bfb534c47038b1f44a519c85`  
		Last Modified: Wed, 23 Jul 2025 16:37:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a22d26f7c4e43335665bc36fca121703bdc16b4cb6bf30210d2155990694321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.5 KB (847476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a63c056bb163e95afc87cb51fe62add83421a277021e0c2dfa95515f80b76`

```dockerfile
```

-	Layers:
	-	`sha256:63ce6d68b037cf9e8c6fd69e195dc051128a3197dbdf2bfb7d420b6ec107745b`  
		Last Modified: Wed, 23 Jul 2025 18:09:53 GMT  
		Size: 834.9 KB (834938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c7146e9bff055a3bded60dde2df0a298a2c44e101257ac1fa08e684c152124`  
		Last Modified: Wed, 23 Jul 2025 18:09:54 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e07baca183e30daec3cdcbc889b097f6f54f4c40f48e0e8b0bf9c6872097e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:8783408c30c7d87a133c97b470eee4b6cb6072904d86ed3bcb0a01b86d57e555
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176887853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b9a266f3a23e0db5f2ce2129d8912a932c67b56cfc9473f702b84e4fbc5ce8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:54:21 GMT
RUN cmd /S /C #(nop) COPY file:3620d5ee3c62a9a7defdfe776efbe134e9eec74e652602e8b680a1191d27cabb in \ 
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:54:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6fa0a5e9c270703af7127826f05971b64e43231e48d8e574f15cab8ef0a09`  
		Last Modified: Tue, 12 Aug 2025 20:55:08 GMT  
		Size: 54.2 MB (54224431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212aebf7ca03b11173fe9d2aeff59f530551fcad130514a7e334c2a3bb884328`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53582a3f4bca191593751e24893d8762fc600a76af2e2797b4b706521522911d`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42da9828e2256a0f08dfc92a2f4127462721ca8932bda3373440095775d1cfb2`  
		Last Modified: Tue, 12 Aug 2025 20:54:59 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:853eb314cf37dc5bead571fd52e07c7271a611cbd1bec848e19fec77d55cda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:875060b1d629ff2fa7a0a9c8a9c712120b573dacf292fc7da1486bf284f74cfc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b0bf9585615a88c24c687d45ade21e5b77835415315e38c70d96e57558526`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:27:16 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:27:17 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:27:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f347076885ded40c10d46a46c8a41531675af1341717251d8d2cf2cc56897867`  
		Last Modified: Tue, 12 Aug 2025 20:28:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafab50289b5b2a42095e99f8e95ccb9ac8364895d938a41a4bb5c03c279173e`  
		Last Modified: Tue, 12 Aug 2025 20:29:16 GMT  
		Size: 54.7 MB (54697384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906cfb424debae93facac029ac7273d434af16a0c5720febb8e1137fad67edb4`  
		Last Modified: Tue, 12 Aug 2025 20:28:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff90e4a3c7aeefd845bea3efc05ab9cdae6e23b13f39b2d934cc116f56f126c0`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1acd00a8475b3da17632d0438701092087f9ada69be46bd7031a59c584a79`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:baa1b677ba2fcbdd9b8a16468ac8658fa34eda0045eb2ca2ee96d0cd8965ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:b850b454cd1c1c6d01665d5439a7d5725f03adccdc7ce6d2301a217af76c5a0a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406bc0a7ea074b91bd504e4ec165c902b9b8da8f58476453c9ca9204f113ecb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:53:04 GMT
RUN cmd /S /C #(nop) COPY file:e7f35439209ec29fad086d717d9f4b58df9184ed229cdee84cb5c209ee80d802 in \ 
# Tue, 12 Aug 2025 20:53:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:53:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:53:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01614d8c42e78a58dcef6b52233a7b481a0541922c151631983a3fd0b16e4e7`  
		Last Modified: Tue, 12 Aug 2025 20:53:56 GMT  
		Size: 55.2 MB (55179587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696fa452e8de21ab6cc0d0c918542ee1831e6d1250ed84f00e993f099957c06a`  
		Last Modified: Tue, 12 Aug 2025 20:53:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d093d691eb644f9d3e3c1867f5245e592f16f8df58f7767cd9f1d1f59ff54b4`  
		Last Modified: Tue, 12 Aug 2025 20:53:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720cd3751519320b63bb908878b5b2ad7692ca12c748a962665956ba668ecf3`  
		Last Modified: Tue, 12 Aug 2025 20:53:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:247c456388728396fda0cb8e500c0d5d83d0624cc364623479cca4cb0fa5257c
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
$ docker pull traefik@sha256:eace18564ef3561b118e8ff545ad8a797d58361120b6d9c2dbbceae0cf346e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57309580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f17a37e9ce42281a054291bc15ecd02405d77302804568ee294c95e5385a6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6a5cdd866efd861489b415dda275d6ce32b233e7eb29b2a9259c65bb5db14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 447.7 KB (447748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac00a37161f2cd17d2443066bbe78745e414c1f89c06a17b8992c1cec3efef9`  
		Last Modified: Wed, 23 Jul 2025 16:33:34 GMT  
		Size: 53.1 MB (53061775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb59abe3b0a1ff06fea7cefb2275bb69f4fa1c26ba5a2ecddfbca1380f2b14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:9aa380b54283255b56637bf35c48c2f6a21caa8ee8ef7c358481e912ecce5e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.4 KB (849431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3debe7e46ccc175361251232da545bb603cfc2e0c6b4d655593d172327b52ba6`

```dockerfile
```

-	Layers:
	-	`sha256:5d0369d1eeb2023fa9f21c7c7fd2e83d56d881638535a956a289269188fa2150`  
		Last Modified: Wed, 23 Jul 2025 18:09:31 GMT  
		Size: 836.9 KB (836893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d7f53175c2f28073e37ece4d4dc48e130e63712c3bd5e132bba61b8b6b9685`  
		Last Modified: Wed, 23 Jul 2025 18:09:32 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3b059ca4a87278ff181ed806fbf657026e327109d6079d80a8c0c4c0cdacbdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52818665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9cebe2fdfc292987e3ce352ac2023eee313a637f075dca309bddd8a00af07e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfa5cb7a6623eef4b1b94d54b62dac25a94d091779e9bf28af0cf01c45ca2d`  
		Last Modified: Wed, 23 Jul 2025 16:34:10 GMT  
		Size: 48.9 MB (48869104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d885957a48ebf1a8a1e1991c221e0db29e865eb0504cab9b026d1a11e36ab8`  
		Last Modified: Wed, 23 Jul 2025 16:33:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:8da48b1c582aa61129a65d0f2ac8be3ea8c2673a181ca7260a48ac74584b94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38327b809aa8068bc122115eaae98758ba03e2b538e26aca37363b1753bd4ff`

```dockerfile
```

-	Layers:
	-	`sha256:0c1d01b03dd1458bb84010574efda803684f13e85a08eabd8e249e4418375bd4`  
		Last Modified: Wed, 23 Jul 2025 18:09:36 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6ddbad673d635cfcc5310a40c5dadc078a4b64d90556a5ab9e197ffe7dcf6859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53266740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd18da0fa25cebbaa78e08beca3e8070d7d69d54e601f00ccdf42a29e375475`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58277fe9b3169f6c6e833dc3c076e6d8cb8174013cfe6f675afb94a7f7caab05`  
		Last Modified: Wed, 23 Jul 2025 19:31:17 GMT  
		Size: 48.7 MB (48686068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9f979bbc32d71453cbbe2751427e6dfbfc3c2a281b309abd387fe1606e76b`  
		Last Modified: Wed, 23 Jul 2025 19:30:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:23e6e27b147c936ad1a393824ae8dbc59e48e0a43bdf97569666573c67f3e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.7 KB (849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b388664c8958e931f7340b10a4dcf06dda25cb8728e640743d20ec8ad1b21702`

```dockerfile
```

-	Layers:
	-	`sha256:330bcf63716e07b7186b61355799a0cf06b0f303b194d36a62225dfa37263e0f`  
		Last Modified: Wed, 23 Jul 2025 21:09:25 GMT  
		Size: 837.0 KB (836985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c89d5d71fbd80b601818f304f19d8982e45ee54bf0459f7f3bcfe9d3e6aa060`  
		Last Modified: Wed, 23 Jul 2025 21:09:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:a81a44141f7213e1b092174f1973aa4fd5f4c3378ea86aa42c0aef77d9a7f5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50979077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de43156b6777f5b6f72104badcdd333f2fa121df66e138057fb8be91d224ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e7a31a18f6e6e899e667847ce220f7725234d795b03928bf3211e58095136`  
		Last Modified: Wed, 23 Jul 2025 16:37:05 GMT  
		Size: 46.8 MB (46801622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02516bbfead5cba4f2b832f27c41cc0df4ce6bb074634717a160f6967fa760b9`  
		Last Modified: Wed, 23 Jul 2025 16:36:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c3484201ee4e7182e642b40d6bcb57af8cf9308c8a6fa008c0ae60600438bdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84a36a92126d60b210234018655172988e3c8ea27eb8475bb27a3e02d6e0a73`

```dockerfile
```

-	Layers:
	-	`sha256:196ee66fd2f4875fabda3d528b89003582ae4086daf819b4dfe7955b5d75b162`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 835.0 KB (834994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c108b88851183a022b367338f8ace2870f73cec93bf01f3b14034663cc5b7cf7`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:2e85387c795128f7ff75629d7e35cbe7206d2eac04fe8e3a8e74b09f3b5d4e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55737852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53367cfc6dacbafdef52b7cefff9e0a369d896ea358dd26cbcd097eb57c0795a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413b15af1ed5672dd303a347ef10c877277d4f19ac5ff5176eef18b3c92e04`  
		Last Modified: Wed, 23 Jul 2025 16:37:35 GMT  
		Size: 51.6 MB (51643924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e671768c8963282ff7f9960c8c83f7bf31991bfb534c47038b1f44a519c85`  
		Last Modified: Wed, 23 Jul 2025 16:37:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a22d26f7c4e43335665bc36fca121703bdc16b4cb6bf30210d2155990694321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.5 KB (847476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a63c056bb163e95afc87cb51fe62add83421a277021e0c2dfa95515f80b76`

```dockerfile
```

-	Layers:
	-	`sha256:63ce6d68b037cf9e8c6fd69e195dc051128a3197dbdf2bfb7d420b6ec107745b`  
		Last Modified: Wed, 23 Jul 2025 18:09:53 GMT  
		Size: 834.9 KB (834938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c7146e9bff055a3bded60dde2df0a298a2c44e101257ac1fa08e684c152124`  
		Last Modified: Wed, 23 Jul 2025 18:09:54 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e07baca183e30daec3cdcbc889b097f6f54f4c40f48e0e8b0bf9c6872097e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:8783408c30c7d87a133c97b470eee4b6cb6072904d86ed3bcb0a01b86d57e555
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176887853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b9a266f3a23e0db5f2ce2129d8912a932c67b56cfc9473f702b84e4fbc5ce8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:54:21 GMT
RUN cmd /S /C #(nop) COPY file:3620d5ee3c62a9a7defdfe776efbe134e9eec74e652602e8b680a1191d27cabb in \ 
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:54:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6fa0a5e9c270703af7127826f05971b64e43231e48d8e574f15cab8ef0a09`  
		Last Modified: Tue, 12 Aug 2025 20:55:08 GMT  
		Size: 54.2 MB (54224431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212aebf7ca03b11173fe9d2aeff59f530551fcad130514a7e334c2a3bb884328`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53582a3f4bca191593751e24893d8762fc600a76af2e2797b4b706521522911d`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42da9828e2256a0f08dfc92a2f4127462721ca8932bda3373440095775d1cfb2`  
		Last Modified: Tue, 12 Aug 2025 20:54:59 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:853eb314cf37dc5bead571fd52e07c7271a611cbd1bec848e19fec77d55cda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:875060b1d629ff2fa7a0a9c8a9c712120b573dacf292fc7da1486bf284f74cfc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b0bf9585615a88c24c687d45ade21e5b77835415315e38c70d96e57558526`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:27:16 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:27:17 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:27:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f347076885ded40c10d46a46c8a41531675af1341717251d8d2cf2cc56897867`  
		Last Modified: Tue, 12 Aug 2025 20:28:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafab50289b5b2a42095e99f8e95ccb9ac8364895d938a41a4bb5c03c279173e`  
		Last Modified: Tue, 12 Aug 2025 20:29:16 GMT  
		Size: 54.7 MB (54697384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906cfb424debae93facac029ac7273d434af16a0c5720febb8e1137fad67edb4`  
		Last Modified: Tue, 12 Aug 2025 20:28:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff90e4a3c7aeefd845bea3efc05ab9cdae6e23b13f39b2d934cc116f56f126c0`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1acd00a8475b3da17632d0438701092087f9ada69be46bd7031a59c584a79`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:247c456388728396fda0cb8e500c0d5d83d0624cc364623479cca4cb0fa5257c
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
$ docker pull traefik@sha256:eace18564ef3561b118e8ff545ad8a797d58361120b6d9c2dbbceae0cf346e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57309580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f17a37e9ce42281a054291bc15ecd02405d77302804568ee294c95e5385a6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6a5cdd866efd861489b415dda275d6ce32b233e7eb29b2a9259c65bb5db14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 447.7 KB (447748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac00a37161f2cd17d2443066bbe78745e414c1f89c06a17b8992c1cec3efef9`  
		Last Modified: Wed, 23 Jul 2025 16:33:34 GMT  
		Size: 53.1 MB (53061775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb59abe3b0a1ff06fea7cefb2275bb69f4fa1c26ba5a2ecddfbca1380f2b14`  
		Last Modified: Wed, 23 Jul 2025 16:33:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9aa380b54283255b56637bf35c48c2f6a21caa8ee8ef7c358481e912ecce5e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.4 KB (849431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3debe7e46ccc175361251232da545bb603cfc2e0c6b4d655593d172327b52ba6`

```dockerfile
```

-	Layers:
	-	`sha256:5d0369d1eeb2023fa9f21c7c7fd2e83d56d881638535a956a289269188fa2150`  
		Last Modified: Wed, 23 Jul 2025 18:09:31 GMT  
		Size: 836.9 KB (836893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d7f53175c2f28073e37ece4d4dc48e130e63712c3bd5e132bba61b8b6b9685`  
		Last Modified: Wed, 23 Jul 2025 18:09:32 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3b059ca4a87278ff181ed806fbf657026e327109d6079d80a8c0c4c0cdacbdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52818665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9cebe2fdfc292987e3ce352ac2023eee313a637f075dca309bddd8a00af07e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfa5cb7a6623eef4b1b94d54b62dac25a94d091779e9bf28af0cf01c45ca2d`  
		Last Modified: Wed, 23 Jul 2025 16:34:10 GMT  
		Size: 48.9 MB (48869104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d885957a48ebf1a8a1e1991c221e0db29e865eb0504cab9b026d1a11e36ab8`  
		Last Modified: Wed, 23 Jul 2025 16:33:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:8da48b1c582aa61129a65d0f2ac8be3ea8c2673a181ca7260a48ac74584b94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38327b809aa8068bc122115eaae98758ba03e2b538e26aca37363b1753bd4ff`

```dockerfile
```

-	Layers:
	-	`sha256:0c1d01b03dd1458bb84010574efda803684f13e85a08eabd8e249e4418375bd4`  
		Last Modified: Wed, 23 Jul 2025 18:09:36 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6ddbad673d635cfcc5310a40c5dadc078a4b64d90556a5ab9e197ffe7dcf6859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53266740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd18da0fa25cebbaa78e08beca3e8070d7d69d54e601f00ccdf42a29e375475`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58277fe9b3169f6c6e833dc3c076e6d8cb8174013cfe6f675afb94a7f7caab05`  
		Last Modified: Wed, 23 Jul 2025 19:31:17 GMT  
		Size: 48.7 MB (48686068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9f979bbc32d71453cbbe2751427e6dfbfc3c2a281b309abd387fe1606e76b`  
		Last Modified: Wed, 23 Jul 2025 19:30:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:23e6e27b147c936ad1a393824ae8dbc59e48e0a43bdf97569666573c67f3e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.7 KB (849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b388664c8958e931f7340b10a4dcf06dda25cb8728e640743d20ec8ad1b21702`

```dockerfile
```

-	Layers:
	-	`sha256:330bcf63716e07b7186b61355799a0cf06b0f303b194d36a62225dfa37263e0f`  
		Last Modified: Wed, 23 Jul 2025 21:09:25 GMT  
		Size: 837.0 KB (836985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c89d5d71fbd80b601818f304f19d8982e45ee54bf0459f7f3bcfe9d3e6aa060`  
		Last Modified: Wed, 23 Jul 2025 21:09:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:a81a44141f7213e1b092174f1973aa4fd5f4c3378ea86aa42c0aef77d9a7f5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50979077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de43156b6777f5b6f72104badcdd333f2fa121df66e138057fb8be91d224ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e7a31a18f6e6e899e667847ce220f7725234d795b03928bf3211e58095136`  
		Last Modified: Wed, 23 Jul 2025 16:37:05 GMT  
		Size: 46.8 MB (46801622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02516bbfead5cba4f2b832f27c41cc0df4ce6bb074634717a160f6967fa760b9`  
		Last Modified: Wed, 23 Jul 2025 16:36:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c3484201ee4e7182e642b40d6bcb57af8cf9308c8a6fa008c0ae60600438bdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84a36a92126d60b210234018655172988e3c8ea27eb8475bb27a3e02d6e0a73`

```dockerfile
```

-	Layers:
	-	`sha256:196ee66fd2f4875fabda3d528b89003582ae4086daf819b4dfe7955b5d75b162`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 835.0 KB (834994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c108b88851183a022b367338f8ace2870f73cec93bf01f3b14034663cc5b7cf7`  
		Last Modified: Wed, 23 Jul 2025 18:09:45 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:2e85387c795128f7ff75629d7e35cbe7206d2eac04fe8e3a8e74b09f3b5d4e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55737852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53367cfc6dacbafdef52b7cefff9e0a369d896ea358dd26cbcd097eb57c0795a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413b15af1ed5672dd303a347ef10c877277d4f19ac5ff5176eef18b3c92e04`  
		Last Modified: Wed, 23 Jul 2025 16:37:35 GMT  
		Size: 51.6 MB (51643924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e671768c8963282ff7f9960c8c83f7bf31991bfb534c47038b1f44a519c85`  
		Last Modified: Wed, 23 Jul 2025 16:37:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a22d26f7c4e43335665bc36fca121703bdc16b4cb6bf30210d2155990694321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.5 KB (847476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a63c056bb163e95afc87cb51fe62add83421a277021e0c2dfa95515f80b76`

```dockerfile
```

-	Layers:
	-	`sha256:63ce6d68b037cf9e8c6fd69e195dc051128a3197dbdf2bfb7d420b6ec107745b`  
		Last Modified: Wed, 23 Jul 2025 18:09:53 GMT  
		Size: 834.9 KB (834938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c7146e9bff055a3bded60dde2df0a298a2c44e101257ac1fa08e684c152124`  
		Last Modified: Wed, 23 Jul 2025 18:09:54 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e07baca183e30daec3cdcbc889b097f6f54f4c40f48e0e8b0bf9c6872097e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:8783408c30c7d87a133c97b470eee4b6cb6072904d86ed3bcb0a01b86d57e555
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176887853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b9a266f3a23e0db5f2ce2129d8912a932c67b56cfc9473f702b84e4fbc5ce8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:54:21 GMT
RUN cmd /S /C #(nop) COPY file:3620d5ee3c62a9a7defdfe776efbe134e9eec74e652602e8b680a1191d27cabb in \ 
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:54:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:54:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6fa0a5e9c270703af7127826f05971b64e43231e48d8e574f15cab8ef0a09`  
		Last Modified: Tue, 12 Aug 2025 20:55:08 GMT  
		Size: 54.2 MB (54224431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212aebf7ca03b11173fe9d2aeff59f530551fcad130514a7e334c2a3bb884328`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53582a3f4bca191593751e24893d8762fc600a76af2e2797b4b706521522911d`  
		Last Modified: Tue, 12 Aug 2025 20:55:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42da9828e2256a0f08dfc92a2f4127462721ca8932bda3373440095775d1cfb2`  
		Last Modified: Tue, 12 Aug 2025 20:54:59 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:853eb314cf37dc5bead571fd52e07c7271a611cbd1bec848e19fec77d55cda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:875060b1d629ff2fa7a0a9c8a9c712120b573dacf292fc7da1486bf284f74cfc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b0bf9585615a88c24c687d45ade21e5b77835415315e38c70d96e57558526`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:27:16 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:27:17 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:27:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f347076885ded40c10d46a46c8a41531675af1341717251d8d2cf2cc56897867`  
		Last Modified: Tue, 12 Aug 2025 20:28:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafab50289b5b2a42095e99f8e95ccb9ac8364895d938a41a4bb5c03c279173e`  
		Last Modified: Tue, 12 Aug 2025 20:29:16 GMT  
		Size: 54.7 MB (54697384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906cfb424debae93facac029ac7273d434af16a0c5720febb8e1137fad67edb4`  
		Last Modified: Tue, 12 Aug 2025 20:28:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff90e4a3c7aeefd845bea3efc05ab9cdae6e23b13f39b2d934cc116f56f126c0`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1acd00a8475b3da17632d0438701092087f9ada69be46bd7031a59c584a79`  
		Last Modified: Tue, 12 Aug 2025 20:29:01 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29`

**does not exist** (yet?)

## `traefik:v2.11.29-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:v2.11.29-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:v3`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:baa1b677ba2fcbdd9b8a16468ac8658fa34eda0045eb2ca2ee96d0cd8965ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:b850b454cd1c1c6d01665d5439a7d5725f03adccdc7ce6d2301a217af76c5a0a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406bc0a7ea074b91bd504e4ec165c902b9b8da8f58476453c9ca9204f113ecb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:53:04 GMT
RUN cmd /S /C #(nop) COPY file:e7f35439209ec29fad086d717d9f4b58df9184ed229cdee84cb5c209ee80d802 in \ 
# Tue, 12 Aug 2025 20:53:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:53:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:53:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01614d8c42e78a58dcef6b52233a7b481a0541922c151631983a3fd0b16e4e7`  
		Last Modified: Tue, 12 Aug 2025 20:53:56 GMT  
		Size: 55.2 MB (55179587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696fa452e8de21ab6cc0d0c918542ee1831e6d1250ed84f00e993f099957c06a`  
		Last Modified: Tue, 12 Aug 2025 20:53:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d093d691eb644f9d3e3c1867f5245e592f16f8df58f7767cd9f1d1f59ff54b4`  
		Last Modified: Tue, 12 Aug 2025 20:53:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720cd3751519320b63bb908878b5b2ad7692ca12c748a962665956ba668ecf3`  
		Last Modified: Tue, 12 Aug 2025 20:53:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:70dae286d3ae856e84305cc7cc1cdd0cbc73d1fd4158845701e6b868ba9e64ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:9971225eda327cebfe6f76283cbee8c64aa29fe78fce7308d28fdf7706c6e818
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75016ca88cd12f5dfa7cb23e18005619b06aa7dec182d13d5b771ef84bed6093`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:28:50 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:28:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9246f832a03d0625295a77b39c6a9f51241182680e05091f53edcd2648a555`  
		Last Modified: Tue, 12 Aug 2025 20:30:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e24f5510416f611ed431d176a07703b8b7cecd5b1afeccb472572f9bd1992d`  
		Last Modified: Tue, 12 Aug 2025 20:30:53 GMT  
		Size: 55.7 MB (55671777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926afb979507dd2cf7ed44703c7160f4c267c76a1e39900efeb6dc3f6e9fa2f`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a29f819c57f55f3c31c6f7d038136bdfbc9fe14f89138541b80c78a4591bdc`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7532a193c37cf8f3b9742e116a8ba96c5e2f73f11f9afe5b382aed9c603ee02`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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

### `traefik:v3.5` - linux; amd64

```console
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:baa1b677ba2fcbdd9b8a16468ac8658fa34eda0045eb2ca2ee96d0cd8965ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:b850b454cd1c1c6d01665d5439a7d5725f03adccdc7ce6d2301a217af76c5a0a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406bc0a7ea074b91bd504e4ec165c902b9b8da8f58476453c9ca9204f113ecb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:53:04 GMT
RUN cmd /S /C #(nop) COPY file:e7f35439209ec29fad086d717d9f4b58df9184ed229cdee84cb5c209ee80d802 in \ 
# Tue, 12 Aug 2025 20:53:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 Aug 2025 20:53:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:53:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01614d8c42e78a58dcef6b52233a7b481a0541922c151631983a3fd0b16e4e7`  
		Last Modified: Tue, 12 Aug 2025 20:53:56 GMT  
		Size: 55.2 MB (55179587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696fa452e8de21ab6cc0d0c918542ee1831e6d1250ed84f00e993f099957c06a`  
		Last Modified: Tue, 12 Aug 2025 20:53:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d093d691eb644f9d3e3c1867f5245e592f16f8df58f7767cd9f1d1f59ff54b4`  
		Last Modified: Tue, 12 Aug 2025 20:53:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720cd3751519320b63bb908878b5b2ad7692ca12c748a962665956ba668ecf3`  
		Last Modified: Tue, 12 Aug 2025 20:53:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:70dae286d3ae856e84305cc7cc1cdd0cbc73d1fd4158845701e6b868ba9e64ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:9971225eda327cebfe6f76283cbee8c64aa29fe78fce7308d28fdf7706c6e818
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75016ca88cd12f5dfa7cb23e18005619b06aa7dec182d13d5b771ef84bed6093`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:28:50 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:28:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9246f832a03d0625295a77b39c6a9f51241182680e05091f53edcd2648a555`  
		Last Modified: Tue, 12 Aug 2025 20:30:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e24f5510416f611ed431d176a07703b8b7cecd5b1afeccb472572f9bd1992d`  
		Last Modified: Tue, 12 Aug 2025 20:30:53 GMT  
		Size: 55.7 MB (55671777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926afb979507dd2cf7ed44703c7160f4c267c76a1e39900efeb6dc3f6e9fa2f`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a29f819c57f55f3c31c6f7d038136bdfbc9fe14f89138541b80c78a4591bdc`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7532a193c37cf8f3b9742e116a8ba96c5e2f73f11f9afe5b382aed9c603ee02`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.1`

**does not exist** (yet?)

## `traefik:v3.5.1-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:v3.5.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:70dae286d3ae856e84305cc7cc1cdd0cbc73d1fd4158845701e6b868ba9e64ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:9971225eda327cebfe6f76283cbee8c64aa29fe78fce7308d28fdf7706c6e818
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75016ca88cd12f5dfa7cb23e18005619b06aa7dec182d13d5b771ef84bed6093`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Aug 2025 20:28:50 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:28:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Aug 2025 20:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9246f832a03d0625295a77b39c6a9f51241182680e05091f53edcd2648a555`  
		Last Modified: Tue, 12 Aug 2025 20:30:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e24f5510416f611ed431d176a07703b8b7cecd5b1afeccb472572f9bd1992d`  
		Last Modified: Tue, 12 Aug 2025 20:30:53 GMT  
		Size: 55.7 MB (55671777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926afb979507dd2cf7ed44703c7160f4c267c76a1e39900efeb6dc3f6e9fa2f`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a29f819c57f55f3c31c6f7d038136bdfbc9fe14f89138541b80c78a4591bdc`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7532a193c37cf8f3b9742e116a8ba96c5e2f73f11f9afe5b382aed9c603ee02`  
		Last Modified: Tue, 12 Aug 2025 20:30:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
