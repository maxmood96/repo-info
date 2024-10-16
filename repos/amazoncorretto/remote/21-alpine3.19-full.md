## `amazoncorretto:21-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:1c6ebc2019f3f15da435d1c4480cf193d8c8a23e06fec4008e6b774cffbb383f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1dfe45a5f7c786ecf5db5b941e781aff8b3b873b8a04d70dd687e2e7f82e532d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162349288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2cb701ebfe8d40be738077ac18802d0e328c33a522aca6522e7a8ed2da4e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c9b5c744d80e7cc5d731829c090d402cf4b6c7af3febcd43c3f760f5e00b8`  
		Last Modified: Wed, 16 Oct 2024 17:57:36 GMT  
		Size: 158.9 MB (158929582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0d48aa5085902a1bef0943215a102c3cff8c2b0d2a30d86e963eb8ed44a4cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4dbd5a048089b78d7be3db3c6090e53682623238f3178fcb6db451f531aafc`

```dockerfile
```

-	Layers:
	-	`sha256:2cda50c19586435beed06cc267995523ba8702286a3e5fbb805351c1a7315a51`  
		Last Modified: Wed, 16 Oct 2024 17:57:31 GMT  
		Size: 381.3 KB (381328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398570b4e4d95a86a42d512fdb69466f90e294efacaf5b06ac59c93d2ee965da`  
		Last Modified: Wed, 16 Oct 2024 17:57:31 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e21ee0201132730f20c5f26598c4ebbb841345ba27d5be5fffd08b64e0d7ed44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160237516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe667e667ab2266fe89085eae82c508baa2c24f9bf37d2ca530122e6721e28c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa8c1f1b4b0cfe6b51ed7cc6e771b479aac5f789b270c02efcb92d72e435996`  
		Last Modified: Wed, 16 Oct 2024 18:37:58 GMT  
		Size: 156.9 MB (156878413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ff376dc762d9ab5ae137020eab1e2aa138277072c2dd8a8978560f465e8bcec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.1 KB (390052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea28b5fee1c9ebe18ddb26298485ecc094d8bf1208ebd5d7fb9838def1f496b`

```dockerfile
```

-	Layers:
	-	`sha256:d382178d1e3a935b632a8debc7ae99c9812804893dcfdb7d87aee713bbf1038c`  
		Last Modified: Wed, 16 Oct 2024 18:37:55 GMT  
		Size: 380.7 KB (380746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8538df2386e7954dfc8c482f4e66a0230a064f8281c4ee4d4dd3123ca5b9fe54`  
		Last Modified: Wed, 16 Oct 2024 18:37:54 GMT  
		Size: 9.3 KB (9306 bytes)  
		MIME: application/vnd.in-toto+json
