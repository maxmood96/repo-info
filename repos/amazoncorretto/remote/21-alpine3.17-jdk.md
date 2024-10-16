## `amazoncorretto:21-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:a205f79342cefe56de146f8ffa18f8ef322f8267cec73f3c1f65b84629645ec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:99f0cc618857f1a32adcbe407c58d3d225cf4dd8de070d2656c0ccff0cbf0f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162321841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc3c07f4dbb2a03e144123cdeaa91c2ae2fdd53c7eef326f7a927cabbed44d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544bd2c8dfaa3ea1ed8f264101288bb17982b697bbb35171d246c1a73eb456c9`  
		Last Modified: Wed, 16 Oct 2024 17:57:35 GMT  
		Size: 158.9 MB (158929647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:05bfc7f23a5f8b87b889f04aa2e9fd527d64fd23fd1ac9defce6037fccb3a759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 KB (389274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e1c0f66f675f548c2a8c25ec3eb82982af866314ac9c8e243b01c628304a06`

```dockerfile
```

-	Layers:
	-	`sha256:777f02d4900dcf5ca686a4160a860977b8b9aaa07212d809e1cbb659a0aee304`  
		Last Modified: Wed, 16 Oct 2024 17:57:31 GMT  
		Size: 380.1 KB (380066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f1c04bc1f69335805e3665e99698acc242706eb717d77ef944f7ee3fdd3257`  
		Last Modified: Wed, 16 Oct 2024 17:57:31 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:901fa5c59e5a733de308bd4e3fa2e1ca39f28570277c431ce04b2b42214e1aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160153525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1497f8cd83ee2ca7bf5cff3c54c993f509b6d3405548932c98ea32b550261`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae142aa96cc6b8db3fb7ccf5cd417003dba5c5b2e258bc268514ed84c1b9eaa9`  
		Last Modified: Wed, 16 Oct 2024 18:36:29 GMT  
		Size: 156.9 MB (156878453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaac0fda31a00e8ad6fc070bbc879b42c5a5010a13d14784991b752f6c2cfe16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 KB (388790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12894a1ad92f0ebab16c031b436f60b82e64ea0a98eae398dde3620b1e8951a0`

```dockerfile
```

-	Layers:
	-	`sha256:e4ba45378d2f35b3152409c3b40267ff60a37c6880476a1fc616ddd5716c4de9`  
		Last Modified: Wed, 16 Oct 2024 18:36:25 GMT  
		Size: 379.5 KB (379484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1868f8d087ded5c8fe49f55a0c4b620cfc4f66bf5ca9ab1a76c4720b231b41f3`  
		Last Modified: Wed, 16 Oct 2024 18:36:25 GMT  
		Size: 9.3 KB (9306 bytes)  
		MIME: application/vnd.in-toto+json
