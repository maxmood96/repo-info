## `amazoncorretto:8u422-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:f1dc07c282ec47815ac0068558b410516984866f5a516a8b9b7b0721d5df2a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a441d8013f8ac8eee82ea276ba7acdcaab918ab25985ca95b5bd3ccaa000b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103515764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd9475dbff459958d91086273294c0531ee34edfe3fd70917b836d4fb75ebbb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf9040c5669929577389584bbc869e4612ffe3489d3130a68590798cec73e1b`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 100.1 MB (100123781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5dc25f36f0430b52724216c3d54a4fe735d4b6d3ae2a71fbd3d61f6e82e91646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f519fd88a5cd258ec1b7a02f3f23de2ae05a51f48faa232e0da0b9c6bce23640`

```dockerfile
```

-	Layers:
	-	`sha256:c41c30dd40b0b6b42a9a45f95069e9a931319ce5729019161767dbacdaf95626`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb078d3c0b3c51da454fa7416855d6dce7ce833630dfbf2bf042d1187369050`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 9.2 KB (9152 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.17` - linux; arm64 variant v8

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

### `amazoncorretto:8u422-alpine3.17` - unknown; unknown

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
