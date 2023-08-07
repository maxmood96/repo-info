## `amazoncorretto:20-alpine3.16-full`

```console
$ docker pull amazoncorretto@sha256:7e347fd5ccf6aba1a873976c2a3d80bbbb41f20f822e833ffef7a73e7c22d399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-alpine3.16-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:91d05ff6705fabea3dc5ad0d88c617678eb0d5a9fa781f4f7e1403bacca59979
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157382383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40964a55813cd74bdd68d18798122d1990c2c6e9bfb227c3817152e6662a6bad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:47:54 GMT
ARG version=20.0.2.9.1
# Mon, 07 Aug 2023 19:47:59 GMT
# ARGS: version=20.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0 &&     rm -rf /usr/lib/jvm/java-20-amazon-corretto/lib/src.zip
# Mon, 07 Aug 2023 19:48:00 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 19:48:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 07 Aug 2023 19:48:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe64069e0971caaa08b5b6e8d74252fedc9082b80ca385b1a0eaf25e016894a7`  
		Last Modified: Mon, 07 Aug 2023 19:57:22 GMT  
		Size: 154.6 MB (154574700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-alpine3.16-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d247dc9ebb64c1c7f1eb72cd76d87de220f1e89b665ff1c83328c9100b6fdc0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155369168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e725cf7ff32170d724e7f41745a395f685bcc6cdb46570917ee6f29876ac372b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 19 Jul 2023 00:48:20 GMT
ARG version=20.0.2.9.1
# Wed, 19 Jul 2023 00:48:25 GMT
# ARGS: version=20.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0 &&     rm -rf /usr/lib/jvm/java-20-amazon-corretto/lib/src.zip
# Wed, 19 Jul 2023 00:48:27 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jul 2023 00:48:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jul 2023 00:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684a2acd1fd98e1cb65ecd35b0a632e9f2380de967df6d4de259a5244f991f2d`  
		Last Modified: Wed, 19 Jul 2023 01:03:02 GMT  
		Size: 152.7 MB (152661262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
