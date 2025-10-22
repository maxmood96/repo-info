## `amazoncorretto:8u472-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:be848298cd91df5b48305da3faaad36582afaad04487d7a1ec137548f3358a7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e7bf2d93224059d2c0942ac9a96a4f8e84155ba53b5d3a3a307ff2ba8f3c61a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104177516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb5d7b7398e8b50fc8844cfe789f5ba33cee549632897cb957e27beb16b9cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825279a409f99e10ef4b96ba5837dc8de52a30d8fdb8e47d2c471ef8cd0cb5ec`  
		Last Modified: Tue, 21 Oct 2025 23:26:06 GMT  
		Size: 100.8 MB (100757701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:35dcc55966c7bd3bcf4c90b60c8c3ab2b56ab1d232e65f4aaec39d1377b85aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 KB (258830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b26f7597e158feb6acb72fad9d67b620f137299760314ea11974c7d7e47be63`

```dockerfile
```

-	Layers:
	-	`sha256:bba8d44f78cd6e63c0856abd1915c1d4d55a73122ebaea73b659aad2ab9787b3`  
		Last Modified: Wed, 22 Oct 2025 00:55:39 GMT  
		Size: 249.4 KB (249433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c062d1f0f0bf63472903b665a8f75a45abc108f703d71a7b6773d07001241b7`  
		Last Modified: Wed, 22 Oct 2025 00:55:39 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:017e6a0d2b153261b79da0e12e5cc6380836fcfa1f4a10d385e42519dcfea480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103892813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2529d92670594ad3d82f1c16aeeb954570e90e538a14c27a65d9672192268b26`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9162e9abe39b5fc833444ff6d32d0bb086e201822afde57795d226a9f7e542c5`  
		Last Modified: Tue, 21 Oct 2025 21:49:29 GMT  
		Size: 100.5 MB (100533512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:11314140747390d7610f056157f4a399f59ce9147bb61f05d6aec61411e89ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 KB (259067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371802dbf3c74667842416905c771795a9e32d75468c3b698cf72f6e1751dd66`

```dockerfile
```

-	Layers:
	-	`sha256:733bcf17430cb0959c3a12b12f309466ae71ac4a1a4af5309067f918128dd25a`  
		Last Modified: Wed, 22 Oct 2025 00:55:43 GMT  
		Size: 249.6 KB (249565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac96b1afb24027ac42434955ef305f6f85e1f19e110510cd422e5281735f8c8`  
		Last Modified: Wed, 22 Oct 2025 00:55:44 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
