## `amazoncorretto:8u432-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:3dbdce03fbe921966033eca64c4f75c949bbe85785ed243e99ed4a335d784bda
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
$ docker pull amazoncorretto@sha256:15f5f9feeba4edef4e9d07831c2ae3ca69c6ba3a2fbd05ef27adc7fb566cda08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44633734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b6e29566c3f20e320a19d55600f9bab2893d293e4669144ddc25c99519f0c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2646ea9f0d852a4573eacd2c0775e8e6aace1b2daf905fe7a422578cea019857`  
		Last Modified: Tue, 12 Nov 2024 11:02:50 GMT  
		Size: 41.4 MB (41358573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7bdec6a4aeddd5210107cb5d7f07263c703a5a4ec14e5f54d0daf919398afbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bf5ba3b55da47e5dd7c0b44e4fd610a1c3f7c80faa19329b72ca64010f81be`

```dockerfile
```

-	Layers:
	-	`sha256:acda60d18a62f93c1654b7f260529b24ebba5008f9c5714492fef3cece943cff`  
		Last Modified: Tue, 12 Nov 2024 11:02:48 GMT  
		Size: 184.4 KB (184370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7391c3c45e8bbce074db46808de53b602c5b1c4d50121cb62d47b00e87de6399`  
		Last Modified: Tue, 12 Nov 2024 11:02:48 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
