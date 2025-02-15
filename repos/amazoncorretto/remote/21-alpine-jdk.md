## `amazoncorretto:21-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:e8ebffa949a7094baf603ad324a4220324bd349d08ca70cad319f9ac036b7e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d4eb1978220a3ba2551e407d3d279bfc77a8903932814a0b4166bbee6588f92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda9333c96c8382ec8566a920fe1b4778812d8b8f5097108369b76cbea998d6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5d56f35012a0efb0cf3144f926e650140b492ee84050727c5057e3319c49c1db`  
		Last Modified: Fri, 14 Feb 2025 20:34:52 GMT  
		Size: 159.0 MB (158955298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:929e328f5855b67c411454a42ca31cc7308a0d79a5e94a00cae681d6d5ad039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 KB (394312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895ec83d3fc2cd29421e567fa9960d0efc1aecd538cd51fc5094eaaf31e285fc`

```dockerfile
```

-	Layers:
	-	`sha256:5abf33a5bafd90470efcba33c903c901d2bc4b440403b60c9c37edf5fdde75e0`  
		Last Modified: Fri, 14 Feb 2025 22:48:35 GMT  
		Size: 383.6 KB (383592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802b13fd04776ae20036da6fc1a4f46390c74a3399e014d1dae5eabd122fa924`  
		Last Modified: Fri, 14 Feb 2025 22:48:36 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:315076929d4f0ef03add2944431b0c80f791c32ccadcb19a863435c37d62768e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160927649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e3956b4ffb190da821b672300c20d7dc39dab1d0a6889c90cb2f335893f991`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:96aada83d83790f5e1e6295c05005003bb6287cc1e27f1d258a9822c644a474a`  
		Last Modified: Mon, 03 Feb 2025 23:06:21 GMT  
		Size: 156.9 MB (156935290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:52fae48a3417c803f72c63248b14167c48533675a9471ea0e5a4f5a664464736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 KB (393923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b5f7d40d1c6b025040bbd552c6f719f63ba275d78c78cfead46ed96398dd05`

```dockerfile
```

-	Layers:
	-	`sha256:0a4da304e1e8f62d2cf447e34de55ee9e8568da6114b98998efd9fcca2196e31`  
		Last Modified: Wed, 05 Feb 2025 17:40:15 GMT  
		Size: 383.1 KB (383053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9346fb7fabc804758a91891018f13b77faf5c1fa7321cece2ace4141946afdf`  
		Last Modified: Fri, 14 Feb 2025 10:03:07 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.in-toto+json
