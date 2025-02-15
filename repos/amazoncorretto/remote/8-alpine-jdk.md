## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:47714492afb84a8b2afcfb9d7d610498e95715d2c828a1d77df19a5db8fabb54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:23aaf5068e534616eb530ca2ef1e9177a0ad00d63a400f51aa4ab5e0b910c4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103866695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c07301d54d0ab38970261421ebeb5fe41edef881629f367fc3a3a6faf87cda7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc2b72ec1b58aebe6bed023c31857d1e015e516b47df0719cf919e75337d80`  
		Last Modified: Fri, 14 Feb 2025 20:36:29 GMT  
		Size: 100.2 MB (100224448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eafc3e2cda43b25fdff1b399a83b2b56392dbf84feec264d345f02f29f78af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 KB (259122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f8c89a9652990259d030d21947178f26d79cb3e397a0f303dcc5950740fe7`

```dockerfile
```

-	Layers:
	-	`sha256:b4ec3ced5b0a6f06b84ac269ddfd2cc0dcc3328df4e8da710cc47d1f8c67429d`  
		Last Modified: Fri, 14 Feb 2025 22:49:41 GMT  
		Size: 248.4 KB (248426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1e2e1f906de8347a92f821101bb14393d6e6926e9631f870660e442af15175`  
		Last Modified: Fri, 14 Feb 2025 22:49:41 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:8-alpine-jdk` - unknown; unknown

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
		Last Modified: Fri, 14 Feb 2025 22:49:42 GMT  
		Size: 248.6 KB (248600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca514925656494d3ff607d0724623c3b9472b7e8f14a6d194b6f8038fe4cc9a`  
		Last Modified: Wed, 05 Feb 2025 05:44:19 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
