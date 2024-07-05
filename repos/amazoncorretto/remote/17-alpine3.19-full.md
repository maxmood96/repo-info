## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:950933535cc7d81fe0851e6b4782f4b25b24a9e3115bbacc77b40c57144701c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0e763fa4969988d8cf0a53b7471be64a8c38b1d81d2bd89f362d387565791a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149653102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d459aa3f206c915cdc2beb55f50efe372bac2a8eff2038ab034003c51d28cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0db5f63c3906482ac90304cf0e89c91fc810984dd49f92dd3a9d8ab4b99878b`  
		Last Modified: Fri, 05 Jul 2024 19:56:32 GMT  
		Size: 146.2 MB (146235770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:410f9b6580e4ebae432039af8b22be73ebf13877aa002001b558f42d4ea06976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 KB (388528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee0c515283a603848709df7ab11b73eedbea14f56bbd7a2e06ccacfa36b6979`

```dockerfile
```

-	Layers:
	-	`sha256:8e694b9254b2fc9aba2857f741c7e0e1d23983a377f78290aebc22a2cc3ec381`  
		Last Modified: Fri, 05 Jul 2024 19:56:29 GMT  
		Size: 378.0 KB (378048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2790491809dce22f8805e4b691bcb2c22cf3b1031970be27c4f479f0ecac7620`  
		Last Modified: Fri, 05 Jul 2024 19:56:29 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:365d1480e712fc7e0fc28bc6b805fe0e90119636a7ea6491b6f896d301b53fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01b7315fa84b079ce0d36e42f1be3c7adbaacbf1eef37bdb9bd0f8a4fb61fcd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7718162609e58e530ed10c8d6174f115f955dcfba9f4ca76240996a7ba3ba0`  
		Last Modified: Fri, 05 Jul 2024 20:19:41 GMT  
		Size: 144.3 MB (144295392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e178decc790be50bcc04e94cfc67e92040468711d0b5289ecc047034d82b508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c783b678ce9af625f860bada4a717ca8c777502c485d008f1c3210a58450ccf6`

```dockerfile
```

-	Layers:
	-	`sha256:9dad5ce6ec5e3a1e0e365a412916b7efcf789bd31241d11b80018a1c2c3137cb`  
		Last Modified: Fri, 05 Jul 2024 20:19:37 GMT  
		Size: 377.5 KB (377514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3751e16bd8a5da6f206607ee69ad6cccd21ef43cb309a0083a2a401c9e7b9a23`  
		Last Modified: Fri, 05 Jul 2024 20:19:37 GMT  
		Size: 10.8 KB (10828 bytes)  
		MIME: application/vnd.in-toto+json
