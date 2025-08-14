## `amazoncorretto:11-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:3fae4397f688fe2c6407e597e39ec6c2225b54cf88ab1a6dec837808c4cf1d46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0093f593a92fade788034158e64bac1a181a0a15faf47e9f797913d8e811e600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145870330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3159c8cc08ca4133fc5ed9e134e9869d6e90f3ed8266c40cae74b26cfc3aed2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2a40bf5868fa0064e6704f8d716ce94fb3597f6f871e30a63e8230ef12aa53`  
		Last Modified: Fri, 18 Jul 2025 20:07:37 GMT  
		Size: 142.1 MB (142070641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc1dd06c992d40ae63284d233dca21fac9389794f35af0ffd1d143740194dae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 KB (403592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5efb445ca0be25a61836e10abf58e535ca1405faed4e02f306274797173251d`

```dockerfile
```

-	Layers:
	-	`sha256:0dcad0fe4d453cd1d44879da63c2366c172f49d2fb69fab36f0a749513e5aeb0`  
		Last Modified: Fri, 18 Jul 2025 21:47:24 GMT  
		Size: 392.9 KB (392867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a952ea2607513fdad842cc55cac3c4b0202601c34f516f0cd33af37c8187ef79`  
		Last Modified: Fri, 18 Jul 2025 21:47:24 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:403f5a5f8fc3ba0244c99915fa2ad36c2074f97f5ecbec6d5e54b7849fb1ed3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144372496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e43af5510e219a0b99817d4551f6044a96638696fecd99df6ad4c23e93c6ac6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01780a726e3de08bd3d82c8b7694e5f82febf68f4776fb3c4e0746fbe9a7c720`  
		Last Modified: Fri, 18 Jul 2025 21:48:11 GMT  
		Size: 140.2 MB (140241746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:77480d4d895651910d1fe0c2455fdb40ea9b3a0f82868655a4e9e92c0a199aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.8 KB (403848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62442d403722ccf2111c27bc40830d5996ae1985a6d2b0d0522f7ece874bb55`

```dockerfile
```

-	Layers:
	-	`sha256:4891b931069ed4543c5270f8b0e14e13ac70b79b5d39bdf0b68359aa32143053`  
		Last Modified: Fri, 18 Jul 2025 21:47:28 GMT  
		Size: 393.0 KB (392971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c810bdebb070f136da3e07847e5a6f9161857c1c828ac969f7ec62412526e84c`  
		Last Modified: Fri, 18 Jul 2025 21:47:28 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
