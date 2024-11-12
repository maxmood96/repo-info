## `amazoncorretto:11-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:a5e8056bb3353ae0e4e9ec2e8db318ac90a2b133e53af049ca508acec4afa0ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:75223404fd4a758f8879e771f76f3159b67ec2dca423378065e5f246377e24b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145329853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7327132cfc9d6d3eaee4833ef4a1d3dd3ce27c5969436824edf967e18e7e8dc8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5138a4e6ca98aa7a3b9cf84f7723bc17c44d9069c5894e7a7f2b94ba6189420`  
		Last Modified: Tue, 12 Nov 2024 02:12:18 GMT  
		Size: 141.9 MB (141910125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7653dcc87b6ad35b247344ad7b2b2e7032a428bca23e27a1002a031dba7087dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 KB (397747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d7072d1356b959f3602c0a44e66952749bab451426a130ea193cdbef51534c`

```dockerfile
```

-	Layers:
	-	`sha256:f40894f5a09eae603e06d21ee76eaa7ed234e6b0b95bd86bd530c619a91cefa4`  
		Last Modified: Tue, 12 Nov 2024 02:12:15 GMT  
		Size: 388.3 KB (388330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78caa7db7c9e1599a8332b6ed291ecd4742e54c89e36b651e488f91bf668f58a`  
		Last Modified: Tue, 12 Nov 2024 02:12:15 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0e5c83c77262a4b01f17b67dd17c2264ec174e6c7da061043c8904557c9b57be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143390373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09211754d96d4d737b113ecc7b71c22b163308e0d832dbf6e09aa435ce379d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f175025c71fe81fa6967a804016bf4f8703d9f31e939580fab33fe0d1a20f7`  
		Last Modified: Wed, 16 Oct 2024 18:18:30 GMT  
		Size: 140.0 MB (140031270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:febff95d4a16541c909e2d2ac5b28290c0104a12688f45847b1a0b32d4d62a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 KB (397601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698088986af2e63d601b8becec68afeeac93259d37c5a45314b0e34a01ea960a`

```dockerfile
```

-	Layers:
	-	`sha256:9729b8da01f2b642a90376fcb41ded411d3f8287dc533c4ae3ddf93380d4779c`  
		Last Modified: Wed, 16 Oct 2024 18:18:27 GMT  
		Size: 388.3 KB (388293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aba1ffeaa092721cb069914c3e9dd694915ef48147e78ad7eb5abe51219639c`  
		Last Modified: Wed, 16 Oct 2024 18:18:26 GMT  
		Size: 9.3 KB (9308 bytes)  
		MIME: application/vnd.in-toto+json
