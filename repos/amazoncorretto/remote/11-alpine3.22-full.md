## `amazoncorretto:11-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:8a2c8c3d4db69f63830e68f9d703a7ffc1d85caedeb7cd74f2e406658332c224
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:82c2b3efb349b9018c9ed13e49ef59507f5dcc4f6652c75b1408f3cf25f526a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147392217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a3bbc1442ed34b3881735f9e7239b133562fa17df227283db039a361d4fc6c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:02 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 18:59:02 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:02 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7185ec7d9ce6a863c3dc1b70709463c789af3f9d73e04fcc94e8b93b673412d8`  
		Last Modified: Wed, 21 Jan 2026 18:59:18 GMT  
		Size: 143.6 MB (143589765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9e2a89d165faffc6dd51e57c52dc13f028d9265e2a588371c1d63ddfb291c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332eff1d540dcce4f481eb98b2dfc1272498f763a5557eb8a348c84e385853cc`

```dockerfile
```

-	Layers:
	-	`sha256:3506af16815fbfb32c0989320aede814315c385a8aaf86ac04440ae17855b5db`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 588.9 KB (588928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c15db3fcee3d1fd3cc5ab39910ea8a410c5b968db1f6cc027b6900086999fe`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:20788ea1aefb0cd4663abf2225a40d1811f464dd3755df2842b521d1c3302d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507596c46920fd28f74cb1a45617fc6508a719f468a20f21e1e86e1231cf5db2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:10 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 19:00:10 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:10 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e383c1903cf3da6da77b9d246d184d2e1d665a7dbe223a71da5be89169745450`  
		Last Modified: Wed, 21 Jan 2026 19:00:27 GMT  
		Size: 141.9 MB (141854400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de4e8be96d4258354255c337285954fd6d0e1f5054f4e616ab3534c3f0b7c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41fff6824728af01eec45b17d070fa421367bd096770fec47a62e80d186aa93`

```dockerfile
```

-	Layers:
	-	`sha256:5eb11a231fc84ea9ca4845d66896b9dcd7b349eecd2eb407d0772088eddfd12e`  
		Last Modified: Wed, 21 Jan 2026 19:00:25 GMT  
		Size: 589.0 KB (588984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e687e9a3b86a435d94295783160215146f983a44f12fc56b58c9a7ae6ec5ad`  
		Last Modified: Wed, 21 Jan 2026 19:00:24 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
