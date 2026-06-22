## `amazoncorretto:26-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:cc6cdd562da006ed8a77be98a529eb79eaf356aa50218eab5b570cac25d18e79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8048936d3176943d5ce769510361b1f04374383be5d93f45257f27fe9a166f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188724976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da864708e97538dd151aac7a6f4d2db9324a2e0dc3cbdc2824895e2857f94bb9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:31 GMT
ARG version=26.0.1.8.1
# Mon, 22 Jun 2026 19:54:31 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:54:31 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:54:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc41c084208d83e82f818a80f82adbd8147db470616c572b2b82f86a9f8e9ecc`  
		Last Modified: Mon, 22 Jun 2026 19:54:52 GMT  
		Size: 184.9 MB (184937381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c467c15fd7664b5d83f3daefc0a947f7153a5742b7b9ab034826489b06bdc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (596968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473ea46ee5c664bcbacd7726c06a37ef42c5fe3cbf8d649633b1a8ab85bd9e49`

```dockerfile
```

-	Layers:
	-	`sha256:44f4993d6dc37f2ed1961a4797f02ebcd386f456cdb7c434c9b71183d54aa6a7`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 587.6 KB (587597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055806b23b24e32e58e5f0faeaf4c2e68e33ae2f810edc3b228b4461171dfc21`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:935c2ef4e38b86d6f281d846812ee2e93081199441ec0b24b2c708385fb2d4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186624317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c05c86b0343a4a0911ac208cc9d3a83fecde64bf48a35509365fa55c7735347`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:08 GMT
ARG version=26.0.1.8.1
# Mon, 22 Jun 2026 19:56:08 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:56:08 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:56:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf97e75b546fd5dda9702524eaefe11152cc9d1ca5e42624223a4db5b38485`  
		Last Modified: Mon, 22 Jun 2026 19:56:30 GMT  
		Size: 182.5 MB (182503831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c30f8cdf54c5cdf5e257f6cdf01d457baa49337eed402cd04dec8cccde917cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28ec24e0aa192327b5091110969fc8d0cdfaded3bce72a1f6fe779fccd23939`

```dockerfile
```

-	Layers:
	-	`sha256:1909dc13fd66498daf184baafc596c9c399c0003ebc0b52ae9c5cab8e9d5389b`  
		Last Modified: Mon, 22 Jun 2026 19:56:26 GMT  
		Size: 587.0 KB (587013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce706a1d45f236aae47e9a14c0e5e2afc7a191a2f40249dc403c058a40b9732b`  
		Last Modified: Mon, 22 Jun 2026 19:56:25 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
