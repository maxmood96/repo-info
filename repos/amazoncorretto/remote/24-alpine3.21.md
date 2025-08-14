## `amazoncorretto:24-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:b4f654c028ec4a1158552ad0500e69a0f57e2c842d25c4ba61c8e26cf993ebc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1cdd79394921154155925472ff36c7521266c9ef43ff2bbcca4f6eb8ae77e583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180408490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1bcae033e65226ff935622025a566263272a7f5ed5b1cd6e825da3a9535629`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd2541bee7d99cebcd26ddb0085f5ec2871d047a20bf4ebb2fb96938f41dc19`  
		Last Modified: Wed, 16 Jul 2025 21:09:05 GMT  
		Size: 176.8 MB (176770920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b040ffe04322874658bca86faffd30195b4d3f7165a127df2e5a835475f884bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.0 KB (405000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3b7b677227aaf8da8e72d582ccd3c391ad1a93c79973992a5c7ea9e49fca2e`

```dockerfile
```

-	Layers:
	-	`sha256:7da4532be1adcf22fd143f726927101f67e244ed4a67d51d4d2d9869b0b4223a`  
		Last Modified: Wed, 16 Jul 2025 21:50:30 GMT  
		Size: 394.3 KB (394279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5474d704b201ba77cf30521d9cec18a6cd645e9ac0b36112c2da9a00a5027b`  
		Last Modified: Wed, 16 Jul 2025 21:50:30 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f41c65d5da6052c9a8096918c1930c58b8d8bdebddcb339ed2933037d20c6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178504410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921b328806b380c14446b6cd5b079b78c95c3ee8c3b84ebaa690b09a2e4fccfa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72184721cc15b708c46b42a2589cc8a2bbf7e08e8b521e3181519fec2ca9c53a`  
		Last Modified: Thu, 17 Jul 2025 04:30:43 GMT  
		Size: 174.5 MB (174517473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1a3b7b2ad4957fc8a470a7a4725360c2124b6238337c5ccb4d478e85bcbb75a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 KB (404616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4373dce99a5013f7c79f44502bab3c3b03d7bbc4458a7d1ae396d5babceaf9`

```dockerfile
```

-	Layers:
	-	`sha256:f9c95e525ebcae252b050099a72d1eb12eec3c33cb2d3226a7366062d254b32b`  
		Last Modified: Thu, 17 Jul 2025 03:50:22 GMT  
		Size: 393.7 KB (393743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee050a7ceb70b62b94e1a251d450ac7d2252f7b723b8bb209062a2eca8494cf4`  
		Last Modified: Thu, 17 Jul 2025 03:50:23 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
