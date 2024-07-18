## `amazoncorretto:8-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:fbd826cd976be014dd0419257fd887107f0a93d34de237e854a5151bbafe1115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bbc56813a4520cc5d71f7592161b0691ebe04c22f9608bc873652397da333a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103541153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8183f59f0bba86429ee6201ade1f05882ca5bd715ead5a140e09d94793c40fe6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc11e65625adf31a7f51d911e1f22827c39726520b4db89ad376c0d457b7b0f`  
		Last Modified: Thu, 18 Jul 2024 00:55:39 GMT  
		Size: 100.1 MB (100123821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:315101702b6f8dac37bcab02d3da42f88b926413c683bab737a7fb8b24af52e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 KB (254888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225426be52f6be3f211d711e8272c0098c0fe95f6054b4c899147c6a53ef0a19`

```dockerfile
```

-	Layers:
	-	`sha256:27300ca5b6cab5f72b061e763b620a0cb27a2b9255f632677e8bcdac1c173b9f`  
		Last Modified: Thu, 18 Jul 2024 00:55:37 GMT  
		Size: 245.7 KB (245735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7fa4630c084792fbc76c7386392bfc1873ad2186aa7fcfb21d4ffc798343e7`  
		Last Modified: Thu, 18 Jul 2024 00:55:37 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:80ef57c5b5641aeff2c17ec772c5e63dfaea2b3fe3903b913b8a2737f2d943f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103193092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ac35af2e9ae97e9b741131a063393c5104d6acd0d508e011124023bc7c78c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32081106161f77061dd3ee08a17a031e3baf43f90a0fb789570807a968d1c08d`  
		Last Modified: Thu, 18 Jul 2024 01:00:26 GMT  
		Size: 99.8 MB (99835890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ce5935c5785e0c0162b2a7f3d445f25622ad6e1d1243e9460bd924dd67fb54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a077de31b77bddffdd5c19e1ae2fca69596b867269f1dbf639af94f3cc8f31`

```dockerfile
```

-	Layers:
	-	`sha256:6f9406394b86c64de558984d8bfc2ddb0c47e7f8cdd5f2b93dfee4002baa157b`  
		Last Modified: Thu, 18 Jul 2024 01:00:23 GMT  
		Size: 245.9 KB (245867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad844c5baab9ea7be17ba78966b74a0d8fd32a458c20a8b372d2c3c97f0f7fbe`  
		Last Modified: Thu, 18 Jul 2024 01:00:23 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
