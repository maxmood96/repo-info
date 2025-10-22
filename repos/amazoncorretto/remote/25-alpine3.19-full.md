## `amazoncorretto:25-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:38a0bf057e03f9d12e3aa3f3b1f2ae96216433899ce9fe51beeaa32490ff65d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:433c8ff1439feac47c562a76b8c884889c1f059d4d896835eff4bc025e917960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184131779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba77f6362afa00ccb5a65844128940e51c175efe4b3f2aa408a65d7cf4967e0f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:dbea97c7e6911ecb1dbf1b14b2cc45da1bfbca01db212531eda2bde825ec8cb8`  
		Last Modified: Wed, 22 Oct 2025 03:01:44 GMT  
		Size: 180.7 MB (180711964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:67aa6becfccbc5b870902df90ad6e7ccc438d4a27105903f46b02e8824812164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.5 KB (603469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec55fc24454cbe21b9d59f6db6112da96de20dae71d01c6bd310f2020cdc825`

```dockerfile
```

-	Layers:
	-	`sha256:6df24b5033eebcc512227ec10cc68be5820d2902327d3643e27fe2f3fd6a1efd`  
		Last Modified: Wed, 22 Oct 2025 00:53:47 GMT  
		Size: 594.1 KB (594055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b51b13bd928f898d2cb35697fef22bf7fb6582f3154fc4dafb6f7415392804`  
		Last Modified: Wed, 22 Oct 2025 00:53:48 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:deeee460541f3e12af3177a4603480fa26cd284e5eb46f219291c0e80f40adf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181732878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f587ebedaaacbd2bca18e622a8f29cb5db862dfb9e166334088c1fc0d5e7d996`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:cd49ff44bf1a9f8f38dced040b0e1d427abb84fd8cf7a4d50aab7c29b62bc28e`  
		Last Modified: Wed, 22 Oct 2025 04:26:23 GMT  
		Size: 178.4 MB (178373577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:326506ee487e79aef7f0982a669aae54ff8d8fb3f64bee04cda465966d6e04ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 KB (602989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4935b784b431259dda7e6441b34c59f4139436d1f7abc76e3fca88cd346633`

```dockerfile
```

-	Layers:
	-	`sha256:68ef88e1450eaed7634ab33e0d0298324c6257367eb145272f3436c9fe4ed73c`  
		Last Modified: Wed, 22 Oct 2025 00:53:51 GMT  
		Size: 593.5 KB (593471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910796a235f8722014c8b0aa24c3e039a2b73c6304f8baa56d8355cbcf48212c`  
		Last Modified: Wed, 22 Oct 2025 00:53:52 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
