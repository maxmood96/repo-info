## `amazoncorretto:8u422-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:8d4d1bc66b094c7d91ad2e8579356ef53abb76cef52e32d2c489ee0b3c60e450
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98aeb096f72be43ad6fa5f0b2b84c74e62cffe235e9b68471f5b37da2850b499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103746661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1044e2fb7a164f80f17a12f76b6aceba188e8ffbd8a7ed9abf8d695827d0c13`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0a7c7308fa1d64a08f426f3e117b9816f3f9bbb7ad79ab8fd2125255b0710`  
		Last Modified: Mon, 22 Jul 2024 23:04:30 GMT  
		Size: 100.1 MB (100123769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:723509ec87e9a12ba9f2e13447c3106b784ed6a933224963de03b00165a4a27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 KB (253249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad50be7cd5675274e058024327a7cf1eea696808fbe5931e9643554ba057ec39`

```dockerfile
```

-	Layers:
	-	`sha256:e8f2b2485a7186816c0fa37f2d0a3abfa9f66f37ed993d88bc108ba361429a13`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 242.8 KB (242798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2290d68a1c5fccdbf135ae82d7645eb25c3b1d0007e816f121de749aaef4bb26`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 10.5 KB (10451 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6a05d74b96551dd2558bf1ae197529c333e5e1292d19e0864570f34085d48b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103921748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec016323c50d29cc34da9d04972cf5a570677529e73e74b1e641401014bc092`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f0bc26a341945105003a0d32c6400f67ebb4815afe0b531e1a808bbc2b61c7`  
		Last Modified: Wed, 24 Jul 2024 16:29:28 GMT  
		Size: 99.8 MB (99834814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2d5a45dd19fa700f54f0cc3aab9589ea4a96a6b3a000fd223c2f9490a8dcd992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 KB (253776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d6ba57480146ede2f33e6f66435971dbcfcd3dcc35a272aed7e0b6408caa2b`

```dockerfile
```

-	Layers:
	-	`sha256:5d68bf2561d79d68c3a3ca581e760c0823a6cbcb508b3501c469facac8bc2108`  
		Last Modified: Wed, 24 Jul 2024 16:29:26 GMT  
		Size: 243.0 KB (242978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a18af9d6cf333fdb604f8a6c88e88b1556ea9fae5ec775895bbd689f53def2`  
		Last Modified: Wed, 24 Jul 2024 16:29:26 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.in-toto+json
