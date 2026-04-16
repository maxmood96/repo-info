## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b39376d21c89b8919a1594602c4a0aa17583f3fad6d14657aa26010b6bb5e2b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:9b1341618fd8069cd95254cb15493e6264f96fa9d1e51884ac24e1056f506beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90080869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766702b597d43b1df3085fd7ae3a7b257624f1eddd2ec9419d0ca5dc1d591642`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:59:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a771a8fbe9b5e998c51ae58eaa3e2a8ab3a71ef4d63ed4482124d6b22b95`  
		Last Modified: Wed, 15 Apr 2026 20:59:27 GMT  
		Size: 60.3 MB (60344371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b60ed68ea1debf8a89a0529027d61339edd0a9c25d7b6b66878da03cd172f0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f46cb677fdd1529459f7db67e65eafaf64812b975681e59e716563c091b73f6`

```dockerfile
```

-	Layers:
	-	`sha256:96f1b2ce0e22ae173a68c8e1e6c0e2e7d7dde83d86ebd446eeb3327740604744`  
		Last Modified: Wed, 15 Apr 2026 20:59:25 GMT  
		Size: 2.5 MB (2547317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64828e3dbc2595827b0bcc023cd19b61be3274dfd49c0df7a278fccb932585bb`  
		Last Modified: Wed, 15 Apr 2026 20:59:25 GMT  
		Size: 8.8 KB (8798 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0e8c5e87eee6b229c3a55022762239ed8ea03b58392672a59a9ffffeccae6590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87104297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d685b5ce0f019c5821fb08d1b8f30a676cf576f3f1b27cab4bf223df3e328f51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:10:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:10:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:10:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2b57434f5d4b0e829f545cc9a095ebaf21040ddb7e3f2690882a296207356a`  
		Last Modified: Wed, 15 Apr 2026 21:10:24 GMT  
		Size: 59.5 MB (59497754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cde8eb7476d949acc05d3405f3f76d5b3d5e247d3b9427ed75162f3006ee2b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd451d0b5f3163f0c7128b0254e63508ff4cfea3cab7181b316c41934507551e`

```dockerfile
```

-	Layers:
	-	`sha256:ff03615a406ca5c68a6ed1f581e23cafb8fd1172b709b43d51f68fb6746b9767`  
		Last Modified: Wed, 15 Apr 2026 21:10:22 GMT  
		Size: 2.5 MB (2546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00330e26e1f6ececb7f5de287d2ec58d52f13606adb02960d900a44e4a3532e`  
		Last Modified: Wed, 15 Apr 2026 21:10:22 GMT  
		Size: 8.9 KB (8902 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:13918d483bb61145ad0b77094feed44cb4135218f1eb6f29e64721963aa3d5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96220915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1598712952c7efe8fb2f5ddfb1c5d4d2080d6a1ad657bce30698f63a5f82103`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:49:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:49:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:49:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b42f0db0a1bf72bf3e885b9a10438f55d6a5339b4a048022d05e845d4a76ef`  
		Last Modified: Wed, 01 Apr 2026 20:49:40 GMT  
		Size: 61.6 MB (61571255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c0056f2301219e123b12fbaaf3cd5dfcaab2ef14e0e08cbcdd7b398c9f9469e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6071d96ce6a991b7c50571e999dc09cb5a0f3a1609db4b2eb02b9c866739fb6`

```dockerfile
```

-	Layers:
	-	`sha256:9c3073586a2aab7c343655810141097596222c768634d07441e0c9db3913d2bb`  
		Last Modified: Wed, 01 Apr 2026 20:49:37 GMT  
		Size: 2.5 MB (2546849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470b94923bd3c8b094bfb8f49ee4cca12f63eb7e735ccb0a6757ab5387c1290e`  
		Last Modified: Wed, 01 Apr 2026 20:49:37 GMT  
		Size: 8.8 KB (8841 bytes)  
		MIME: application/vnd.in-toto+json
