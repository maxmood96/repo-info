## `amazoncorretto:11-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:9bd211789858c9df51562fe74d08fa0265ca8083904936f468c98bb8b6165f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4cc29ac5daaba01943a3db87c7acc8f59f07c546b2548c739801ba6470c00af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145532477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1efd8aab5730258b876464dbca315267ed6fcd24fe316ce9416f1acc6001aed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc15fe49ff02bbce36a541dd23d01fef2936d1be54016fe5597e319bf13e12c`  
		Last Modified: Tue, 12 Nov 2024 02:12:09 GMT  
		Size: 141.9 MB (141908573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:319201c23b610299752dcbf1b7b2266db0c8e2812232ec618309513f407a5af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 KB (396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe8a4fde5607ae2a2a9e6e84e0a8dba53a47a7bbbf9d100ca69aa482a242a37`

```dockerfile
```

-	Layers:
	-	`sha256:64c51a61dfc6b2a81f1eac96d4bc20d56eed9f6e41303171023929c9d125ee17`  
		Last Modified: Tue, 12 Nov 2024 02:12:07 GMT  
		Size: 385.4 KB (385403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11e2fe7e6df5466f6328f38ab9b3f0725e5eabc7de509db0df844d7ee4f61ca`  
		Last Modified: Tue, 12 Nov 2024 02:12:07 GMT  
		Size: 10.7 KB (10724 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0cb9f15f31c81301a8a601c898a465d75df5f4d27e8eac12accafd6b02519ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144118439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af176dd956b30b6e62ac0252be4d76c6d41f5e9c5e3a22c14e06fc86beaffcf7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feef5f54761e4ac1e35370a37a80317ad13c13520a484a79788aab6fb52a56f5`  
		Last Modified: Tue, 12 Nov 2024 11:08:13 GMT  
		Size: 140.0 MB (140030713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:132398796a08101675598aed6fab7d5e9718b15be9297dcff63a34cf2087ab50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 KB (396384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f5e941b36d89e77d81645cc383b960c888e1992f9bf3b9dda171fcd0491cb8`

```dockerfile
```

-	Layers:
	-	`sha256:91c733bb0e8a7d9c6caa3c595c168dd17c9d6ae28c72ef26dec663fb20f28ad0`  
		Last Modified: Tue, 12 Nov 2024 11:08:09 GMT  
		Size: 385.5 KB (385507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43762d29cdc1935bd4056994bc85765b6435703986dcf220e12acdee0549d06b`  
		Last Modified: Tue, 12 Nov 2024 11:08:09 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
