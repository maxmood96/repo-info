## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:5f34a557b6fcf090c05c018f6a2d408db60e5ea085b79530b69440d471a30ad9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5aa8f6c713446ac0cc730c80419d5bd9ed5cde3e3574f152b00c341dd93e0484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103809160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a571726e1fe4fff10fee79d5e0a19cf3667688394377644632bc99d97e9131d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23e43e6f53084bf3510b05ccef4cd071b41ae953296289e0049a62aa3ce93b`  
		Size: 100.2 MB (100195161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f323b22ce2a025fb2a46a8e35769c6bf8ed631209f75c9bafdf42ed5ec6bfe3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 KB (253396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2a78c0c9504d39c6b185a52b34fb1b9ab40531d30ad44cb6a8ee0b764968ea`

```dockerfile
```

-	Layers:
	-	`sha256:9bfb0b95e760912c02cf4c29d02a3c13de4005f1c99794e37b0d9a04101efa4a`  
		Last Modified: Tue, 07 Jan 2025 03:28:44 GMT  
		Size: 242.7 KB (242700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7754ad77202538fe0032d6514b565a0ac39e9d27ff884dbb6acd1d65a0b4463`  
		Last Modified: Tue, 07 Jan 2025 03:28:43 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:afe2402417725524da70b07d764b3ed1a5c1b1fc75516b06aa0136e2a0fb3978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104065458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4dee45ddb5e6ff5500d728f3ad6e6fe2945492b0afe642180b4e3140e94832`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33cff45b705502f7f0f172cfb49c9089c2cccc4dda47602929fab71e1087c6c`  
		Last Modified: Tue, 07 Jan 2025 07:20:33 GMT  
		Size: 100.0 MB (99978772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e7e7d517352f0c80bcc04f17f001c35e022e8fb11aa7388ae1023307b2ed2896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 KB (253727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d43850264dde6119499a904d64190c3d738a4d6db18c191df0feca16d9f050`

```dockerfile
```

-	Layers:
	-	`sha256:21f9be636b3b96fb4b3ec7a52f6b9e0edb032d55d8f9f3c5939dee9e6cc0d0f1`  
		Last Modified: Tue, 07 Jan 2025 07:20:30 GMT  
		Size: 242.9 KB (242880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f9da1a91be0018eebcee8d215abd4cb3b20cbb968d207aecaba297c0737cbf`  
		Size: 10.8 KB (10847 bytes)  
		MIME: application/vnd.in-toto+json
