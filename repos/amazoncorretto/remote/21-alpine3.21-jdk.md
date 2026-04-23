## `amazoncorretto:21-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:447a2beeb12fd6e017849ecf56954067f8586a9dfcf1fbdb10083170a1615118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a9b2df3a2e24a50dcb277836f2588e1b668b41ecd002034a2d4d7c1efefb5e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165457544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e232a7a014a129a9ccea1b2965e6bcc0738949e0e6ed5bb67aac257cd9c5b16`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:49 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:49 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:49 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd468438c6e41bed3543de320f5cb1e93ebdcac5f7f0ca5f56f9c55c39c726d`  
		Last Modified: Wed, 22 Apr 2026 21:35:07 GMT  
		Size: 161.8 MB (161810669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d18ec6cbb9cfc0eedf86be35e3d7c428da29e4c8fffa0c346baefc7d14d3265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53abb0eb355e30ba10b61b8482a4fe6c68fceda8e03ffa3ca83bb14f85ab9cc7`

```dockerfile
```

-	Layers:
	-	`sha256:74ec7d815464301f459ca43f0266388d0998ab334d3a618e2e795efcde0599eb`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 587.1 KB (587112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35751868ef23b735f123bcd105c45156fca413906c1443c04f17d19009851ee8`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6de9b39225753cdb0d8840aeceddad3a5a67c62c8434b0ada7e1eee7b6d5b303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163813560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3336d5c8bf972438e0cdf7ac1d03cb782e58f066f0ef9c9e103810ee64c4b62f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:44 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:44 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d130066541a2c29f051e564dbf422bde112f0d20c866b616b747f3ff24ff9dcb`  
		Last Modified: Wed, 22 Apr 2026 21:35:03 GMT  
		Size: 159.8 MB (159819095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:508613e78ed3baebc7c30f3ed9f6892903954af7e97a462a4d11afc024cb647f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.0 KB (596014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819bd70dcaec21a1391fe430c8d4297ae6aa4b12196a63bbc5d841d3ae8b5798`

```dockerfile
```

-	Layers:
	-	`sha256:9e4cee4ab30d12372cf6650e3df8be055d71ce6244cc187f08d0dc0dae5e993a`  
		Last Modified: Wed, 22 Apr 2026 21:35:00 GMT  
		Size: 586.5 KB (586531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927182e393b570e94e41f103462307faf4071d570226a86442a9924616dbd856`  
		Last Modified: Wed, 22 Apr 2026 21:34:59 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
