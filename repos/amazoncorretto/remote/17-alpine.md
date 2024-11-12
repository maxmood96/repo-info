## `amazoncorretto:17-alpine`

```console
$ docker pull amazoncorretto@sha256:05757d999c5aa507df8eda99b53c441c54ef7117e390c7b75f57b6e8626afd3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dbcffe2592f5c982faa0b8673f2929f8af2f5c66f1bf05c23774b1a0db0c36ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149273136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f98983210cc0d0302e756170fbbafc343e3e7b192adc10a084b7096bed7b08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:2b1287f8bbe94da22a0ba0f4f23024ecf7a226be38072a54e67112db499b925e`  
		Last Modified: Tue, 12 Nov 2024 03:14:12 GMT  
		Size: 145.6 MB (145649232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df8e1d58222622b72d40bdb2897729c03237b1cbca01eccc5a98c393507879e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 KB (389327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01bbd2a4bb7d4b518649f2133baa0271be87e84b3d2f37daf3c9f3435ec8477`

```dockerfile
```

-	Layers:
	-	`sha256:a899dda8714e39e49fd6add6954d9eba1b4e196f3f34ace3c3c9fc7fa79364f5`  
		Last Modified: Tue, 12 Nov 2024 03:14:08 GMT  
		Size: 378.6 KB (378597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57073993774f283ef1edae8ae118568409f1f77913c8356b1e7b93d9cee4b5e`  
		Last Modified: Tue, 12 Nov 2024 03:14:08 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7399db70d7f7d048cd4af62a2cafe0307b94b87d64198afbd74dd4583549b9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148022279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbfe10caa20df3a2914790bff2eb45f0742f8b96ded255170681dc67c78419f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:644f628d973a703645cb2f2b4a6afac3e28403d169cf5a085cecafb375b39792`  
		Last Modified: Wed, 16 Oct 2024 18:30:37 GMT  
		Size: 143.9 MB (143934633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8b1ec0ce66f829f4f918559b61993a7bc330f5862830b44a6ca9ce30136fde60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a5b55ad8ea1bdd8640649b4d61d19b1c135ece9826d113ad16048fb0b76761`

```dockerfile
```

-	Layers:
	-	`sha256:63d7e6f9da3f97a7f9692cd66f74c83a3a594687dc29d27a9ee8c70378a61644`  
		Last Modified: Wed, 16 Oct 2024 18:30:33 GMT  
		Size: 378.0 KB (377970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff948cc16ecab608609c5fc039b48ba7250c59cf9e4344c7ed3d74ccd676b6f`  
		Last Modified: Wed, 16 Oct 2024 18:30:33 GMT  
		Size: 10.7 KB (10668 bytes)  
		MIME: application/vnd.in-toto+json
