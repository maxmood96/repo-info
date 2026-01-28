## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:8a49dcb14aa4098ef0eddffc17e8e1b486040b6d93c28aecedf73f67a368085c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b1f617f94dd0b54f5c5ccbb95ed69bf21d015ee6a79a3b735e505e856d124831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a848d8d585ae1c855c096959414bf316c46881f8acf3aef69ccc75c330544c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:24 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:40:24 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:40:24 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:40:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbcd30cf2aede157c58c52c3a5cff221dc086aff9c63656bee43dbb136a5645`  
		Last Modified: Wed, 28 Jan 2026 02:40:34 GMT  
		Size: 41.7 MB (41742909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d494782adfad6545298cc0d8cf674172c645b77121f4c8eecd76274aa6e8f1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c424c3e42e49b1f7d8cf6a0a8c455ec030e9883cff7e8a2ed8cb28d7dcae3ea3`

```dockerfile
```

-	Layers:
	-	`sha256:1430383f55adaef2917014f3181f6d80c2d37f07865dd7d6b685cdc716c9a950`  
		Last Modified: Wed, 28 Jan 2026 02:40:32 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bea4138d773d86f682cfa0662c089cf193e41180b47e6f42300c736d2580a7`  
		Last Modified: Wed, 28 Jan 2026 02:40:32 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

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
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4af095a24aa3d8930abc8943d254dcc0951fd3884882ac53ce1ee0b9ee3f69`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 41.5 MB (41458246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

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
