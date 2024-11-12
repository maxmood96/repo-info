## `amazoncorretto:8u432-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:367c249490192ebafc3ffb15aaacbc5dccd5bdecf2debba19647389c0d125e21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9d93d5b34c03861f08ce28b09c5f9afc708d560e7e84a6b5f83f126fdd79f992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45047830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e675b465b04e02612dfad69b13b3614427fb00c34b8e7952804503f5f042a37b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d80e970926219e814c98132fd2dcf0a88c3d0147d6cd36df9219610bcbe69d0`  
		Last Modified: Tue, 12 Nov 2024 02:11:46 GMT  
		Size: 41.7 MB (41655578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4c31ef242e78e2a5450cb83272e65b2ee1f32804ec080a80c6da0bdd7794113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec9b1d2cce8b230dc6c6bdc3e3718d35062fb3c4580dbcd2d2bc7767208d950`

```dockerfile
```

-	Layers:
	-	`sha256:e9b7396b4929c953c371cb509fa8f4a43c9c21e1d9ed97585d621ac241ad4b53`  
		Last Modified: Tue, 12 Nov 2024 02:11:45 GMT  
		Size: 184.3 KB (184262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d531104103d477c6a7b920c8f80e02daa27b0d7482c4719f9a211578d60cf725`  
		Last Modified: Tue, 12 Nov 2024 02:11:44 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9367cad8016073196443dca6c55e8ecbcd3f6572a5e4cf521819ecfd80132d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44633698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72a5c0ee802d22b8fe8a51aee133096e46f6b27ea1b19f19d3a4c6a8f60be66`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6d3421120f41e2f520aa9b2c40bb295c29f9165dc829bd35c69cc44a5547a5`  
		Last Modified: Wed, 16 Oct 2024 20:29:24 GMT  
		Size: 41.4 MB (41358626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3818620c9c272bf51258046f79fde1a3064f5156ce98977cfe162978eaf480df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c67292d1b0ae1df42c143eb804f590e17b629a996494ffd12cc27e51149e02`

```dockerfile
```

-	Layers:
	-	`sha256:298dba43bee6ff78f8af69c04a6a20554293a9368a52e4a60ab3ed273619ac6e`  
		Last Modified: Wed, 16 Oct 2024 20:29:22 GMT  
		Size: 184.3 KB (184277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2157c125335d3d14b8e7a0b9669454db4f0d7cf92b240dd0979716e9df73925`  
		Last Modified: Wed, 16 Oct 2024 20:29:22 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.in-toto+json
