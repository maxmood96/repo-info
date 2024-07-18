## `amazoncorretto:22-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:a1d3852928eb3d2d0ab8ae5e15084cb40d03f285a44e4aa68d1bfdf5c04f7ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:226b890bf4d03cd6b41fd5824d8cde0ca8631295c9fd9e00b279c7dc27f67b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160986257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361d44f9d2d7afbbe5f7c950e19125033182cfbaa072fbaee5a76c51b6024b86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c16781a5e52b772f37826acc83817395f140a858c309228e3b349b1718a95`  
		Last Modified: Thu, 18 Jul 2024 00:56:08 GMT  
		Size: 157.6 MB (157596294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eaedaf08793647b93224f5efdb1f480d11d91a26b72f21fd1417fb651747bf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adf12e0f99360078ed9f7122d286444e07b9d8b1c239d37d95e21de38eca124`

```dockerfile
```

-	Layers:
	-	`sha256:334c7f611fe9c9086ba426297008219d3c3f3d5851dfcebe0c6b0db54a63ffb7`  
		Last Modified: Thu, 18 Jul 2024 00:56:05 GMT  
		Size: 380.6 KB (380644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893ca8650ab8975fc02e711b9bbbaf09c96f2d1955ebdfb717a4f6a5e7257dd9`  
		Last Modified: Thu, 18 Jul 2024 00:56:04 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d665f7c6abe0a12d0ec49dd30be5ad8751eb18cec6f1f1de2294176f52303049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158467266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcee4f45343320dc6bead0aa913acece5945027d18437dca69d81dbf2589d94`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957a16b128ba58cf230a0e70f29d0a33401028ae10c834f84cf7fdd9a2589ee2`  
		Last Modified: Thu, 18 Jul 2024 01:28:46 GMT  
		Size: 155.2 MB (155194680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f1614c9d74094fd0f3450dd1d077403cf0eb87c0b9046a80f9a87e90fd020cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67ceff0d327c6777c5093b1b17efd8b8c871c8b56da86ebb3d9c6a4380e5a87`

```dockerfile
```

-	Layers:
	-	`sha256:c8bc20bbee15c29504dc9ca270205420381354b0f1a29622ecb36c798a2ce0e3`  
		Last Modified: Thu, 18 Jul 2024 01:28:38 GMT  
		Size: 379.4 KB (379421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39ecc84bbedeea410dc7d4670efea5a671c704090a510e20932929e791c1f7f1`  
		Last Modified: Thu, 18 Jul 2024 01:28:38 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
