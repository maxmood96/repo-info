## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:1cfd8dfe5708781534e02b7d246724abef8ccc09f8220504aedac6ad3a914625
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7f19792d7901973b27c5ec575d4ab6a3ac98333af8e58a7190c3b4157a8595bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103588144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850648d76e286095ec87b7c540da600da78cfdf067e004826a10605b7805b442`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5eaf3c10fb09ce8c1743637305627b50fbca3bbe6c68996cbb1f3e5d9551e7c2`  
		Last Modified: Fri, 05 Jul 2024 19:56:21 GMT  
		Size: 100.2 MB (100170812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e308a0fc1827741ef5dcbfe83ad9689ac21187477081f634d96f98dceacb5595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 KB (251107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccf14d65bf16cb3b90f84b66d3f5494df1a9c91c8e7bf2175fd830a963b1bef`

```dockerfile
```

-	Layers:
	-	`sha256:38f4f0d359899ee66ff597ef7e5600dee45af0a22e478ce6b24bfdda97e089f0`  
		Last Modified: Fri, 05 Jul 2024 19:56:20 GMT  
		Size: 240.7 KB (240656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705ee8a7f2d7aca3e7db02bafcc0e31aad03721d902f9de54831eef08bf0cfd5`  
		Last Modified: Fri, 05 Jul 2024 19:56:20 GMT  
		Size: 10.5 KB (10451 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b1751e5ccc80289af153a90f965b3805d9274d082fef38446e968ad512b872e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103176460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0862da053f3ce53c294f0aab76bc20206955f6ba6d2fa30db436391e1fa21e2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:7feec6cc69d39822e2c6dbde4f5ac35b6be14796a77af505def1f12920215c99`  
		Last Modified: Fri, 05 Jul 2024 20:02:12 GMT  
		Size: 99.8 MB (99819258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cdedefaacbee6211a7f5312d985fec44be17c96fb4ab91d9fc2402005963b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 KB (251634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e1e9d450c96df8a41efe9c0f6db3366c3e634148191ab97ffdd18e43f33ffd`

```dockerfile
```

-	Layers:
	-	`sha256:87483d6b0131a40e2fb11db8edced731131d0716d73192e50b972ab66c98c54f`  
		Last Modified: Fri, 05 Jul 2024 20:02:09 GMT  
		Size: 240.8 KB (240836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb55f7c302934ccfe233ad0b5863fe5d4db5184cd9ebc2bdfcf95520527010ea`  
		Last Modified: Fri, 05 Jul 2024 20:02:09 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.in-toto+json
