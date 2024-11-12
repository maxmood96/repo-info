## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:e88ac84b286524cba25f22ac6093c0aece88d125fe31085b10bd9fe543b6a845
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-jdk` - linux; amd64

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

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

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

### `amazoncorretto:11-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a8cea4011a2910ebaf1314205f156eaccac0778450e9f28d00aab7d13fbd13b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144118437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07827b80c9b53644fd5e6948185d134a6e391a4533002c411c250b7a17ee82c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d75e0b84f6a291f6a433e35e083f59f3d0af9f4e372a4ba452f6ad81e4ab3e`  
		Last Modified: Wed, 16 Oct 2024 18:19:12 GMT  
		Size: 140.0 MB (140030791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:99a4afebd171e3b72e55cf6ee7b27081a8b30bcb9cce9aae2df6e470af624fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 KB (396078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddc02b826f93b211dc7dabe3c6b5349a5b624f1c4f450765936f60f4fee3d4`

```dockerfile
```

-	Layers:
	-	`sha256:25951ec21b652e22c3bb191b1c55db3ce20f435fe65c2b7ea9c3f6cbb8966b07`  
		Last Modified: Wed, 16 Oct 2024 18:19:08 GMT  
		Size: 385.4 KB (385414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a209a7c402a13f05b564456bdcb1669c82f6f2ff1282ed6c6e6dccff3bee6c`  
		Last Modified: Wed, 16 Oct 2024 18:19:08 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.in-toto+json
