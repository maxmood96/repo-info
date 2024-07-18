## `amazoncorretto:8-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:98e2d0500cf155d36bba2bad46e21e3cdbf1e290171364bb6b9f0eb45f9e82bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3d046ad43edbbc63300aa86573ed24c6db671c34f10448aae59469d79e6879b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103513665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d104a04b0f28ae047acbb9b97e2749682a233e600e23e8f9f6cc1a8f27a9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
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
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d379f8090b2ff9718c60ee0689057d0220cfabe078df5544b53f8c29ff80cf`  
		Last Modified: Thu, 18 Jul 2024 00:55:33 GMT  
		Size: 100.1 MB (100123702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d3e13ec53430434800a4ccecb1f94c195489d04b3db6ed3d0f0b2889d1319b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ee0e7de31f07e65d4c441cb8965b9d1aba47c201585857bbdc2ba5f490bc45`

```dockerfile
```

-	Layers:
	-	`sha256:12b646a9c1d6cac61489ea767bde97f920ef6007abbb7204c90bf6af6dc89db9`  
		Last Modified: Thu, 18 Jul 2024 00:55:32 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588d45e5fd5c829020433177a5f1a843ab56c0fb504b04fb2c56d1a91392f735`  
		Last Modified: Thu, 18 Jul 2024 00:55:32 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d47617df293eda0858c6aa061a63d69b121ba6819590e5adad2e11661e68ef32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103109207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d854fd7db37d75bf2f56c0bd57f8c3e8df432ce904b380f58fa09c67abaeaf1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
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
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30901e297ae08c26e78e28aa5fba2dd0f9c91efd9a9a94ab0a900090cfbf900`  
		Last Modified: Thu, 18 Jul 2024 00:58:45 GMT  
		Size: 99.8 MB (99836621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0f69a6dd954406dd1a4c182df3d5cea4f63e2e0ecfb4d610306abbed18a1049e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 KB (254057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1db327d477a2b7bba30cb191120d8b9933f0e575581a8ca2c4a979e442a41f`

```dockerfile
```

-	Layers:
	-	`sha256:9d71a6fe197a3e82f54f1a81fc6376f9e5c6ccff107a816bf854af20eb78b180`  
		Last Modified: Thu, 18 Jul 2024 00:58:43 GMT  
		Size: 244.6 KB (244605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c864b4135392f9427ded7705fe1b2493a9845c935e5d544125a4b4bcf4e3dd9a`  
		Last Modified: Thu, 18 Jul 2024 00:58:42 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
