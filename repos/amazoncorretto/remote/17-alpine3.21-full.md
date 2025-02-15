## `amazoncorretto:17-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:3c621ceb6552fe0fc2feba76370d5b66d7ebe16931c1b43239f1888c80cfd919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c57f2a61fe3dcc37dbe91f4bff81f2ddcd3cb10bceb39a3f2fd41b89df4f0e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149320802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f9c68599d35742cd96478cae1087a03d571e938519205188ec043144fc67c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:584747a5efa75c554a1694422dbb83cd51737c9345280744ae0fb36f23bc0ca5`  
		Last Modified: Fri, 14 Feb 2025 20:34:49 GMT  
		Size: 145.7 MB (145678555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2e60b04955ce8a7ab4e1bafac6465122c91d8104f913dd3e3cadb214c5811fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 KB (394420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c002efcd066b25af86f4590cb44a400cf6f1b08d0c5bcfa4d9d6f1d6538b6435`

```dockerfile
```

-	Layers:
	-	`sha256:61cfcd9ef0c056bce976ed892f6b90fe82f2803ead58763862871b0b10eaab6c`  
		Last Modified: Fri, 14 Feb 2025 22:47:58 GMT  
		Size: 383.7 KB (383697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45cea0d15c0ec5735a02bd45965f8dad23f7698f5bcea2f2e8875ec47b1a033b`  
		Last Modified: Fri, 14 Feb 2025 22:47:58 GMT  
		Size: 10.7 KB (10723 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ab9a3d3a47a5bd0d8e3ab3a7d7308000da1598f415a381e969fd2f20563ad36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148014195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04da508ebb3930853243db3df9051226c4f0cadd2f555645064ce898c506f865`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:348becf58d4a829afb236b35cda7a76ffd8e670535b8cdd58811b7a59f0076af`  
		Last Modified: Tue, 04 Feb 2025 01:01:26 GMT  
		Size: 144.0 MB (144021836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b58082f7f3d48a02ae20d4522419349b3ffe501826f0257cfa6253565fb82a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 KB (394035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebce5391bda895032216239481f9ef7b3af25ccdca36889b0c06671ba594f817`

```dockerfile
```

-	Layers:
	-	`sha256:621d3e039c52b1b22e1db5b6f3755bd7193a9bc81c409add73af61e525da8e87`  
		Last Modified: Wed, 05 Feb 2025 17:40:20 GMT  
		Size: 383.2 KB (383158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beeb43ccd8008e60a193b7de95ddc95fa96b547448f8b9bc960bc6c03670424c`  
		Last Modified: Wed, 05 Feb 2025 17:40:20 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
