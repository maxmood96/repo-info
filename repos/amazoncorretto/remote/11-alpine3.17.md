## `amazoncorretto:11-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:36492bf9a3aa8dcaadbc19d30b016b89fcf7195ee685663aaa4da6b0450ba4c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17` - linux; amd64

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

### `amazoncorretto:11-alpine3.17` - unknown; unknown

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

### `amazoncorretto:11-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a1f413ab2f80e8d2ceb366a1f11468fea924dd1b95ee5140f038b7eb5abbb36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143231183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d940c7fd659d223d19b126212dcfa99b4df6d940d7634d3b56e2716d4ef0de7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
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
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbb2b020eab5693303ca895083432a6509e9b9dc2d5fac90b1cb898c8b7b8a8`  
		Last Modified: Thu, 18 Jul 2024 01:07:56 GMT  
		Size: 140.0 MB (139958597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e4ef1b2a506a6b5fbd0cdff5d4314d3ea922df5eb6bab18b7416958210d82c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a702d10a3d9af2098235b598b5ffa95e8af4d02be988795dfd87ba29b5fd27`

```dockerfile
```

-	Layers:
	-	`sha256:a571713d4b0a0f039e09a11e05d8666cf8d89e01edb7c71f17d1888cd7d9a7c2`  
		Last Modified: Thu, 18 Jul 2024 01:07:52 GMT  
		Size: 387.0 KB (387018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32921453706ed13e8f8c03e474aa5258aafd184af07a89b283e708be7ba8ce6`  
		Last Modified: Thu, 18 Jul 2024 01:07:52 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
