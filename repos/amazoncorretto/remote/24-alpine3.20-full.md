## `amazoncorretto:24-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:fc5a56d120dc1c96f896b784bdc6b3295228c857a01c30df5253efccd502bfdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:46d7c6977873e5b352f15eb8a83f133777293c06b9fa643404e0f198e9597dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180229775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a1d00dc9e804bc052fbaad5f39d6fc8c3621b67304eee80f2f501bade9816d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06180867a04566e5966773f240622100a492f334647073fc84c5e82cff04dd14`  
		Last Modified: Thu, 08 May 2025 18:27:42 GMT  
		Size: 176.6 MB (176602878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1e30226be59eebcea1cd3965bb85b38a38c209ef7960b9566d85d089335dd49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 KB (395066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc03760fa9ba0644603ac43dfb2a4d7b029b9a46a99652a624fb6d2356d26cea`

```dockerfile
```

-	Layers:
	-	`sha256:4d5fcef5e2b93d8403d53037fcff73a449f987bb7a2752ea3ce8c2bf46278c68`  
		Last Modified: Tue, 15 Apr 2025 23:56:00 GMT  
		Size: 385.7 KB (385652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff094289dff3f143e25f3e6796a8e9c4697543a2ee9292ab1ad6641c6fe6334`  
		Last Modified: Tue, 15 Apr 2025 23:56:00 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c2c557d1c31a8ce2daeb7b214cacd79972a834c4390e8eb50c9827be414f9fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178394281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deae57fdeaabd96782f0f76a5700828c74175a310f15fbfb9fe9caad7316470`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536ad2ecb7f6da0b75ac65356c524cb2ae77cb3e2b97821ad64837217ffcf479`  
		Last Modified: Tue, 20 May 2025 18:24:33 GMT  
		Size: 174.3 MB (174303116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9ac11156005881ce270ea959c6a57a94da8bc148e4cc13603b255648a900468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 KB (394586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173315fa4547ac23b720f28df2b48cf5bb5925451c1c41947ba80cbb30eee2a2`

```dockerfile
```

-	Layers:
	-	`sha256:bf8dc0463d9032167d663ba01a9dd8fa0e2cdd5ce262724cbdfa4aa2769a83e4`  
		Last Modified: Wed, 16 Apr 2025 00:24:45 GMT  
		Size: 385.1 KB (385068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf547cef2aeb79c9ef280a8434277b5b8ebae8616ce372fa8aadad6721463d06`  
		Last Modified: Wed, 16 Apr 2025 00:24:45 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
