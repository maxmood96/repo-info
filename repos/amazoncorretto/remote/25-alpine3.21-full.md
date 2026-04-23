## `amazoncorretto:25-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:dd8bbad51e1a4fc8e0445c80762b4ae531fcad027f0b5ac7db80d2e1690b58c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6057a2a8ebdc36b044ac62727b311b8a40371ae23e91a7b08fed3f59ef864b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184642300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9365ec52ebe82c9c45ac0b0ade76cf8cad41b024b7117a12d78751f4528be3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:20 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:20 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8879614fa6e0076b0569cf21e22a985c25afc1e0a09b9f390a30b5985c1dcf67`  
		Last Modified: Wed, 22 Apr 2026 21:35:41 GMT  
		Size: 181.0 MB (180995425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a35bbc1c3ef48f031f4f8d4dcdde753455ee817a109e0730c7fa35a41a7263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 KB (605577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c628a59aef11e82e4a0693570549dc4f7d24c0dc433c2016310844da49a118bc`

```dockerfile
```

-	Layers:
	-	`sha256:1496c57644af55f529106000bf26b3f9794227f20f87e78a13db179806feca40`  
		Last Modified: Wed, 22 Apr 2026 21:35:37 GMT  
		Size: 596.2 KB (596206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08ee8b81e1fccd089dcdbaee022132c9064679bbc06280dea98952be31dd639`  
		Last Modified: Wed, 22 Apr 2026 21:35:37 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:633436ab5a03bae5ded1a022c19ac51644c11daecaa2ab9a53ec1bc6e371b115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182609539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69e55c227df083cc69337b57d16e10d4aea43a00dffedc30517f0b80eac1a2e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:16 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:16 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e884019749695685cf858c85cfdb7b33ebdc989320c3e272d283c4feee4ac1c1`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 178.6 MB (178615074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bc2897f241e134cf05193c0cbe8e9445d0fe99aa61b83bfa09fb7273ec3f93df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 KB (605097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858b697359665827ec0ef879bfb146832745ecba0187bf7b1bf32046166800ab`

```dockerfile
```

-	Layers:
	-	`sha256:317e1d0eda9c532b5ee70786dda347e78222a32d7282411f7e9f279b92d4c496`  
		Last Modified: Wed, 22 Apr 2026 21:35:33 GMT  
		Size: 595.6 KB (595622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b46ae21ab448b4050a25337fad67b3ab154351f3bc35b28e59dd05820f295d`  
		Last Modified: Wed, 22 Apr 2026 21:35:33 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
