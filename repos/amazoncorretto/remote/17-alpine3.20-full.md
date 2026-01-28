## `amazoncorretto:17-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:faac5ade8c82e34f0b25951f775dc60dd0c807329f53a62a8abbf38b1308d47f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:da318a66b5a788019b28fc1a90f126b2378bd3825c97c37d8a091b0de51167d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151984377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6f6fa6f79d6e3a8f0aa9881ad71a317a30c810dad733fcf601c58fd23dd945`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:43 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:46:43 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:43 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6e8dbd3233b7d7af30b245552ec88c7e31afb14b905797784902c404c1e780`  
		Last Modified: Wed, 28 Jan 2026 02:46:59 GMT  
		Size: 148.4 MB (148356513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f5ef77c9d29a72e5dece961f268c6f73de23046da53dcdea60c67fdfaf69941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 KB (590028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57398026ce0ed2d8b8eceae66026a1f6f240c0b5b1b45318cc78978a9f95157`

```dockerfile
```

-	Layers:
	-	`sha256:1e2ecd05dffd7ca607c0b9171a9d234e8a4c6e3b238f2c89ef91da4772788ae7`  
		Last Modified: Wed, 28 Jan 2026 02:46:56 GMT  
		Size: 580.7 KB (580654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833710b696193c4146eb5d3223fb9391f8ab2e5eeb5aeb97190b5313ff5f7954`  
		Last Modified: Wed, 28 Jan 2026 02:46:56 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:833c4ef12b991736066b6b34133dc2918b8d2186cc4a904390fc8f3ccc797fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150807263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d7217a129ae9619f7c7fc53278219b0e7340d8720d0e4db5ef889036195b7c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:44 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:44 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:44 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22626b56812b3ffdc5010724316f6f597a1d1dfe0d9895dac6d9d61d9f97a335`  
		Last Modified: Wed, 21 Jan 2026 19:01:06 GMT  
		Size: 146.7 MB (146717886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f000a2e09fffe2a6f66cedf9bb28c642d00c721a0f05857a31fe211cc4a2140c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 KB (589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0721d9d7716210efdf5615026b264fb668c51071110b55d185e9876134edc271`

```dockerfile
```

-	Layers:
	-	`sha256:40b7e55fc9b622b52ae885351d625bb15de5132ba0ccf7fdb0f5995bd34a5c17`  
		Last Modified: Wed, 21 Jan 2026 19:00:59 GMT  
		Size: 580.1 KB (580073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f465c225efb1ec562be39589ca15108248171a9a1d3cc64d4922f4bdaeeba80`  
		Last Modified: Wed, 21 Jan 2026 19:01:08 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
