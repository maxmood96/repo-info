## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:0015bb4571bb2609ae6070c87ee35a3a1c04ca6b70ca845b69b53e06c8ad1cf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6f1a2f70616c9b7e198d14b44bd4251bfc238d0355e7e0c7a9e990a371fe0c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103866124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce240e2a3d4cceebe53a75dfaec93923eb98d3d8db085cabb0fef0eca921950`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a6ce8261665c77bbb111b6283cf23d0a069f611bcf5a4fc474c7f16073f8e2`  
		Last Modified: Mon, 03 Feb 2025 20:40:58 GMT  
		Size: 100.2 MB (100224409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f3063767cd59a80ebe54e4859fd5c0992ba9695d95a53e28716ba6233a9697f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 KB (259116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c28ca89592df04c9feeae1fd37a14dbe5e369438ba4299cd76e58adac07abf`

```dockerfile
```

-	Layers:
	-	`sha256:bf4c7f68130e646dc68c2d26ddf6015dd729c5917bb0b8e6f812d6cb217a3f90`  
		Last Modified: Fri, 24 Jan 2025 23:26:17 GMT  
		Size: 248.4 KB (248420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05a45baae8d239865de9159e9094fefbe0d1e0884ab0e17f0c4840abccbef99`  
		Last Modified: Wed, 05 Feb 2025 05:44:20 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8f7136244544d430b67e23f9ea27d659759c0fb7e20e30413b6ae8cf1966113c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104001451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f33efa502458ba35b90ee26019c7e17057f431588151f245e572122796b371`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138417d13daa22c6cc12a75838baabad16a7f9093ef076866c298184d1f24973`  
		Last Modified: Wed, 05 Feb 2025 01:15:04 GMT  
		Size: 100.0 MB (100009092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17e6588642824c75d709351efe9a527928db7582e8059aefd1fbf62ea52d5368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8a8a0f04624d3c7cc6b9e484a3d1f70852c1a5761ae4db65f5356611937467`

```dockerfile
```

-	Layers:
	-	`sha256:99ab9485752dea427630f38e133d044befb5ca4b654d55b5c8e9bbfd57de27d1`  
		Last Modified: Fri, 24 Jan 2025 23:26:37 GMT  
		Size: 248.6 KB (248600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca514925656494d3ff607d0724623c3b9472b7e8f14a6d194b6f8038fe4cc9a`  
		Last Modified: Wed, 05 Feb 2025 05:44:19 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
