## `amazoncorretto:25-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:9a039625e2b20aad96aebba0214a4e2b7057913e18064aa8e236219e80453e8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2b7b7003c28957ce7ddb8355e61f6a7ba765f0ee4175522c3be3abd49ad21990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181945399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e87dcc2e3910df86f9062a04862433f16c25f71728e3f635b0cc7466835411b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1f135cbbcdd0e859bae4e873e9b552fb6b89d8342a31f51b062d59e690cf85`  
		Last Modified: Wed, 08 Oct 2025 23:00:57 GMT  
		Size: 178.5 MB (178525584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62ec7819e3ed19285ed437d134cd6623156d4493053479d84f66180d598f8e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 KB (400894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aca3dd07d4af7205bd26be87a7354208d23fb1ccbb326e4b4af3cc123a77a2`

```dockerfile
```

-	Layers:
	-	`sha256:132d89b22d091ef06f99ca909a7c23b04081683b74886a357f0d500068d20be8`  
		Last Modified: Thu, 09 Oct 2025 00:51:57 GMT  
		Size: 391.5 KB (391479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c5bf31859fbcb4fe8306e85da38aaef9ede3aabd6a78e00128aa9ab75fa8ec6`  
		Last Modified: Thu, 09 Oct 2025 00:51:57 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f5344f24fb562a9d56adbafa65fe0480a2cb6e4d79baeaa124ce7dac27aeea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179431930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7db9d5337d1f71fc7ec59a366c69558ba3e002448c801f0b19d092528be4f33`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ceda43fb45dc68376b19373e90811c448a85c6b8ed180196866bfeb7100521`  
		Last Modified: Wed, 08 Oct 2025 21:47:57 GMT  
		Size: 176.1 MB (176072629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bcf546e49439bc7349b1b31dab2097af2fc21418f5bf3af04c53af8f0c0f5a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 KB (400414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fa7da475dcfce16570da0bf9b277be1b30246aef53461d5c0c9f660c9823e8`

```dockerfile
```

-	Layers:
	-	`sha256:83e3af9c70e6a3aa392016ad1dc25af3a11eccef7c14a73ae75186dec4726e74`  
		Last Modified: Thu, 09 Oct 2025 00:52:01 GMT  
		Size: 390.9 KB (390895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed894ba76806d3bc671495b6b9d3d0c9f14069c17f4bc681719b1536d5e08cad`  
		Last Modified: Thu, 09 Oct 2025 00:52:02 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
