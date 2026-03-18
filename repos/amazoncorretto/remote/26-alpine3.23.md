## `amazoncorretto:26-alpine3.23`

```console
$ docker pull amazoncorretto@sha256:d36d71e81652d2511080598d4e12bf9757f22b4661833092201bffe9b37f5819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.23` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c43ff74cbcf4a36cf04b5802100da3675b718263d267b642ddbc862ff6cb8bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188780860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed17158571a3f5c2f4e7c66622a5eab2020f90dfef763598936d90594709223e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 23:01:00 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 23:01:00 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 23:01:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 23:01:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 23:01:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2788af7130a4d19993701ce7e9e36c7d300f186310d740ddb1e54ee0f8ea6e`  
		Last Modified: Tue, 17 Mar 2026 23:01:20 GMT  
		Size: 184.9 MB (184919039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f5c67fd622a865b75f20dd484be45e6e75fb34aa5adce74d43118bd70820e2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28844d0a49f9740b9d4db37e7ed3a5721b4185ce9bd6c43a422ec25a1d0c2fe9`

```dockerfile
```

-	Layers:
	-	`sha256:83ff54cd638e720b8e8846c3f0ea654048227f9dbfeb2d71d1bba6c94aeec74a`  
		Last Modified: Tue, 17 Mar 2026 23:01:18 GMT  
		Size: 587.6 KB (587585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d996daac8ab099b50a671f8d47ccaa8391fa9bed1ab1c642951577317e9abbae`  
		Last Modified: Tue, 17 Mar 2026 23:01:16 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:88c381f1d13616a740f91d6fbf3f2899fbbbec3985fa65ba23646fd0f0f697d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186685222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd0e126f5f75fa0e73555bec4e93180b9cc0e510077ab66e789e45e84aad943`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 23:00:36 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 23:00:36 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 23:00:36 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 23:00:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 23:00:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c2ac3099f0fdc39db1f2b10185205414c7c479f0b8a0dad6ec6a43550a354`  
		Last Modified: Tue, 17 Mar 2026 23:01:05 GMT  
		Size: 182.5 MB (182488131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ff4b16f0038c05fbfb684f6ce0f1ab33ec496b75610f1f4aa207c24a67e2433e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 KB (597229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae800c84c32de4a1f71c5537be680b69cd48e3d5f966d6c328935630dadc17`

```dockerfile
```

-	Layers:
	-	`sha256:7cd1ce39ac4b2ba9ef1ef61f0947226c1899db6809ba24746bee3c29563fef94`  
		Last Modified: Tue, 17 Mar 2026 23:00:53 GMT  
		Size: 586.4 KB (586399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f67924e96d25c495accad36dc7bdbb055c992dd8158e307f2d09886ae3b4ab6`  
		Last Modified: Tue, 17 Mar 2026 23:00:54 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.in-toto+json
