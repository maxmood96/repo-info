## `amazoncorretto:8u442-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:6f77f4efa0b88d1eb10d63e878ddb6c19e6a1606e26f75787e623fb4d85458e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:10764fc9a585700ff5dbd5c03eb10d9167e3350b97c47ab2b93f3430ddb8bcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45281710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2a875349cccd08f2b7cceca1975a0c22efb46234c553661167e460b1ab2be7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe3316568af26ceca7b8a13f1b5f5038c90fa62e92da452377d1a2a81a3cc0`  
		Last Modified: Fri, 14 Feb 2025 19:12:27 GMT  
		Size: 41.7 MB (41654813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df8f69b6171c491c63898e9b0fbd77846d6146bcd49b7db55f9487d944dfe320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 KB (189799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae0976de134f216abff0fe729c27f607feb98495d66fb35696a6f32af0a1158`

```dockerfile
```

-	Layers:
	-	`sha256:3d0a4644b30100f929fc5029bf6bf559b03d3ce53f7bbacf327846e30b36b7f2`  
		Last Modified: Fri, 14 Feb 2025 19:12:26 GMT  
		Size: 181.1 KB (181101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46a26e8f04c2f18451ff5f1be61202692824cd163e70da5e8a716465a152d185`  
		Last Modified: Fri, 14 Feb 2025 19:12:26 GMT  
		Size: 8.7 KB (8698 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9aeb3940e628a1bc4ae4a07fd804244854033493605cea8de3da058dab0ceed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45452859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67acee57a86ed46ebf08883dbeb6bb9a7278cdc01dff179fc59855739d4a46a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8fa03804a09ab976f5663a9e0ba746b3f258fae724f349e47791e013bdcfd0`  
		Last Modified: Fri, 14 Feb 2025 22:33:12 GMT  
		Size: 41.4 MB (41361694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:949ebbfbae34302559888e14a1e11706b6d86afe2079df96e56f92403e3d8426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ba31fde37154e50daa7b91124966d971ef78d178f34a171080ada9f9cec2cd`

```dockerfile
```

-	Layers:
	-	`sha256:dde41fb0d5aefe7841fcb111d006451e89681fc46bd53e68969740061edd34db`  
		Last Modified: Fri, 14 Feb 2025 22:33:10 GMT  
		Size: 181.2 KB (181209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de368746dd4d54c9bfb4c216d6dc98a3221425796d4647360e7c7e3d2bb80c11`  
		Last Modified: Fri, 14 Feb 2025 22:33:10 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
