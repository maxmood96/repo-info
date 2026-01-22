## `amazoncorretto:8u482-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:4acb0684084e2197b85d8553cdd91a701867283ddd395d74058ca19c03caa32e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bdcb1d382a3f9cf96aeca28ae68aa6bfcdbbf1bff94a9b647f2dc51df94e20d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45369973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6ac796d4f929211583479f979fcd02b2612b2636804dff996acb9690905ed7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:13 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:13 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:13 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3ebec4ced57c1c0267db6df1f5e83b62a805f6213a2f21cb7d598d12dbd832`  
		Last Modified: Wed, 21 Jan 2026 18:59:24 GMT  
		Size: 41.7 MB (41742917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93944449a1538eca1aa25194a6ffec83ba339546d16359fb8b5767fe05ca1993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d4bf956cc9e42603734ec8ddfc063c2de6f81d4d79b8b437b8f88db71a92c9`

```dockerfile
```

-	Layers:
	-	`sha256:d2d08b95f391804efc243df9f021f13e83dec7bd2890022677b02e5c8be31033`  
		Last Modified: Wed, 21 Jan 2026 18:59:22 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8acf9911262bcfa1bf008b3c517ae864febddd39d0bddf6f01d03a4f6a041d2`  
		Last Modified: Wed, 21 Jan 2026 18:59:22 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9576481ab6a64e9d10dbac815c86f0ce65d4d70084b5ea44bbad9f84764210e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45547623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abd8406525de983fc2305985179f0660afd30db10b91c7616e9b7f78624a88b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:04 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:04 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:04 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4af095a24aa3d8930abc8943d254dcc0951fd3884882ac53ce1ee0b9ee3f69`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 41.5 MB (41458246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f7e9e5020b4f94dcc29d6933a81beb704d6d61c8ade4c36f8be28ff90acc15ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 KB (191662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a27c1e0cd7b0a9b24b3c1d3ba09ce21d8e62599aadbeb3a4f24db4a87a0cc4`

```dockerfile
```

-	Layers:
	-	`sha256:c8feb4ea78ba8a33d62e46c7101c4c66ae9b2c44c4486c848ff457f8e2e36919`  
		Last Modified: Wed, 21 Jan 2026 18:59:13 GMT  
		Size: 182.9 KB (182926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f402ea2a87b2d8ea04ef6bc0762e8e8f79a16d1023a7da4b29d080dee35e6c92`  
		Last Modified: Wed, 21 Jan 2026 18:59:13 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
