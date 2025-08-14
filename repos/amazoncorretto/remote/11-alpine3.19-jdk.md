## `amazoncorretto:11-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:03a9349d81af030fa736246976e8125774e8f1697720493f3fdab014cf469b36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8b0c00b6d5e159495512bc88e59e4838f2b960e7a4220c6b660c263a2504f773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145485996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c4db0e54821ec9ec6f920851416e0571c288654c04d2cc46776af9063dfde2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=11.0.28.6.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084f1d2a6f6f0fabca876c582e6f093e16519a769142c370c1d5056831caf089`  
		Last Modified: Wed, 16 Jul 2025 23:29:42 GMT  
		Size: 142.1 MB (142070468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:70983ee5b1f6348f4c4b13391c108652c3e2b90e27b3a07c261616d97b6f5679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0fb70535a6bc3e9313a941efb2c4e76427a91d47ec90d42f0c4b2aa37f748b`

```dockerfile
```

-	Layers:
	-	`sha256:76a5e56284c94a308138eb6de8b46e99f49a952e27b72d3166fb4ad192ad2403`  
		Last Modified: Wed, 16 Jul 2025 21:47:53 GMT  
		Size: 389.3 KB (389286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3f8c04bab81b6bdf06c2ae6f48b567442446cd1ea3b1843a247d20dada8014`  
		Last Modified: Wed, 16 Jul 2025 21:47:53 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:404ab12dd3e9baae22787adaa6512222e59e56df83a00e9d19832948c2360030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143594806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7835911f45a6a74755634078218a5907b2994e4a146dbc424d486e343bab758`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=11.0.28.6.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27f215c17e9b6ee9b303777cf82fb0b7596a8d644418e0e4364b7afc594eaff`  
		Last Modified: Thu, 17 Jul 2025 11:48:52 GMT  
		Size: 140.2 MB (140241703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b1965e221c0271fd921bd5667b270af689df54debf3c2866f15c2ee3734f5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 KB (398863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae30cd639d1a3a6bbb96271630d7d9a62bed5efbd2afb8cdb5723b9424044696`

```dockerfile
```

-	Layers:
	-	`sha256:18c7cc9e010322a6730cde90fbeadf6db2712dd1be9606dd3361dd6229677a8a`  
		Last Modified: Thu, 17 Jul 2025 03:47:48 GMT  
		Size: 389.3 KB (389342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a82beb27f38ea54e1bcc39f3fecdf03ddc7190f2b8122772df0be427928332d`  
		Last Modified: Thu, 17 Jul 2025 03:47:49 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
