## `amazoncorretto:11-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:1176b19d501eb72609fab4059bcb0afa9a86b6a8a3c93d5fa20103dd1cce321e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:15b3b7129d6681f3d05ba6b4f9cb57a0618f162ae4f6c8a6d196264eb4d19372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145202859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935e181b7ec361abd9a833b8d22a2e339c3c7371005bbe2ad1bd37ddc299a802`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:ffcaf8f123bf07a4818690782ec4ee424b22811f6d7fec39b17c143a0da007fa`  
		Last Modified: Mon, 22 Jul 2024 23:04:44 GMT  
		Size: 141.8 MB (141810876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e0ec6839aae2738ab32bc1e63d48f6eafb923715a1a897a1fef8118d6f6f250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 KB (396134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1249422b9aa69172aab63ec65f970ac3695b2089b83372d9bb0a626b9952c731`

```dockerfile
```

-	Layers:
	-	`sha256:708561487ede42e257e7864ab957625ec98a870206ab9f517ba2d1af7ade4ea3`  
		Last Modified: Mon, 22 Jul 2024 23:04:40 GMT  
		Size: 387.0 KB (386962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7289d621844d413467c9ae96ef30886908c432592bc6be8183ce4de07387200a`  
		Last Modified: Mon, 22 Jul 2024 23:04:40 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:51f0ca468241af0da2a0d15e93b9dbd216481036df41a565fa9d7c6f6379bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143232899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f84a1aac3a280c5241ac6c2132e12ff8f5d428469ba3949a3b1e20560aeda0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fccfa8778150b3cb538858998fbbfb2b5633e19ee5d8239576f2b956b935a7`  
		Last Modified: Wed, 24 Jul 2024 10:40:05 GMT  
		Size: 140.0 MB (139958654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28f63542b95a54fa422a598681ba6c87196f11fe9f142e5add539e9ac9c5e672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c17c48e493e67adbd4c86c5258630eaf42408af79223e043410d20d5250711`

```dockerfile
```

-	Layers:
	-	`sha256:7e5f13eca9aab6164a24cc539f9be5c126b30fa01d8b85a8c863dfe0a8b53313`  
		Last Modified: Wed, 24 Jul 2024 10:40:01 GMT  
		Size: 387.0 KB (387018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25fe9c36e8bdc945b42cc871243535b21a8533be7a9f03448da81a040e6079c9`  
		Last Modified: Wed, 24 Jul 2024 10:40:01 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
