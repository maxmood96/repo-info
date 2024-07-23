## `amazoncorretto:8-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:a4ea459c7977cffffe5c7b34afa45d8eb338ac155c5703314e5322fae7419e76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dad57c3eba3e25dd16b93c3a9cd4cb0fd5f9bd2cbf006b454a55d5c20400c1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103542783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc82cde5b005e8fb6e3bedeaca851f97d58a115aa5d2147e5fb71230f320510`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe692b3dca96388b35ab3a20be36084c0f29144fba2899034bba12fbde3d81d`  
		Last Modified: Mon, 22 Jul 2024 23:04:31 GMT  
		Size: 100.1 MB (100123743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de7d4e1381146251509b5a6b603380a334cb4bfd29a8924e54e9865246a25f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 KB (254888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bab587b48ca248ce7e73e1be296f99be5a1cb1bbd9e5033712a1a79c4545702`

```dockerfile
```

-	Layers:
	-	`sha256:15d3678659394f74c9ce84812c406f30b37a38f301333146eb3c48e09cf9c386`  
		Last Modified: Mon, 22 Jul 2024 23:04:30 GMT  
		Size: 245.7 KB (245735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5fa439f231ad409aaae11c1311b07a81c0556892cf2dffd3a3b7e6c9a18d03`  
		Last Modified: Mon, 22 Jul 2024 23:04:30 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-full` - linux; arm64 variant v8

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

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

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
