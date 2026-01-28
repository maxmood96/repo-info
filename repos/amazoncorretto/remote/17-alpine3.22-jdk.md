## `amazoncorretto:17-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:e72fc609041435ffeee08c5780dfa3412876c13a05c303163481046928084ab0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11d30a24c48c44be64873ca9f076c6c5b8f33d3a2e2abe25822b70d2fa171f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e749f90964e12fb2a06b6a244eddacbbfba86b9a7c0713d3c89ce29d66f2c6a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:40 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:47:40 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42553a5753a849b2187e2fe6d8199a6666cbf97cab10ed6414555b01a4a3764d`  
		Last Modified: Wed, 28 Jan 2026 02:47:57 GMT  
		Size: 148.4 MB (148368550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0d3f9f26da56922e7e89c91f2ee2e610cbf26f98a313361fb5d3be16b039f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.5 KB (592510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44120a187729e0a6417c6781aae9689dfa61e9a1cb2abace6ec1b62d3283a17`

```dockerfile
```

-	Layers:
	-	`sha256:6862a9b10a61a13b49779ef97bd3cef8ad9c867337959f67332b03e44aef477f`  
		Last Modified: Wed, 28 Jan 2026 02:47:53 GMT  
		Size: 583.1 KB (583136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e55ffd355e8e076f5a2511271ae963d75d05fe8aede4ccce38bec971fe5bec`  
		Last Modified: Wed, 28 Jan 2026 02:47:53 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9ff1135258eabcbb74a55749a34132509f479bf0e0fefb6ebf1be94b05c6a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150848734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d671d415240b0309b38a565bfef01559f710667bf12bb76e491895572846c3a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:01 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:01:01 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:01 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde3140e10e11e4387174d07cddb8aca0009a035801366efa9ae13ed4e7e6b8`  
		Last Modified: Wed, 21 Jan 2026 19:01:20 GMT  
		Size: 146.7 MB (146710665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e5348845b70930ca02f05c9f25c303270d9b17572a45203f080f28b979c87c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 KB (592033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713e9e4c26266e95a2841ccab50719c2ac7fe63697e920c0a129cd7c61d57d41`

```dockerfile
```

-	Layers:
	-	`sha256:bd9d620c530962e4e3b749559bdc1e78c857266e5752a2171d92a41e97f8b703`  
		Last Modified: Wed, 21 Jan 2026 19:01:17 GMT  
		Size: 582.6 KB (582555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c3a06ea8b164a6ef03df4bfe0dff568ff0f33417fd8f2bc4d7100305fb07d9`  
		Last Modified: Wed, 21 Jan 2026 19:01:16 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
