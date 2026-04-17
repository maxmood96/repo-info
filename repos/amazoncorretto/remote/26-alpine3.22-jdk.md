## `amazoncorretto:26-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:5bf561c443e1a2dafd70f4c93bba28ca1b55138e1d6ba3fe2fa93ac8f19a19d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ede159c48ea926aef6c69aaa8f637aa2c1994c95ab61e005f1af26a84bbaf26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188731347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8457d8af8b77b3370a7699549ab9083d835a61a04eeb3cd0f677d301d73fa896`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:25 GMT
ARG version=26.0.0.35.2
# Fri, 17 Apr 2026 00:23:25 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:23:25 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:23:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:23:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33924b79d77e7ecd81de67795ba6195bfdc2ac90275be76bc53ed5a614fdc1c1`  
		Last Modified: Fri, 17 Apr 2026 00:23:48 GMT  
		Size: 184.9 MB (184923158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48704b032d62eb7ad357425e2a576f955f9c3024881e5bc096bd2bfa08eb257a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (596958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128698b9c6925fbb03f1861970e96a063b31fab5d850e53e097a9f23f6fcc3e9`

```dockerfile
```

-	Layers:
	-	`sha256:218068bf13cc8e4fec96dcb2375df607f19ec98cb19e7e44bb892111a552b8f2`  
		Last Modified: Fri, 17 Apr 2026 00:23:42 GMT  
		Size: 587.6 KB (587586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0f7eae511dcf088c73574d8ee2d5e2787b7ec9afcb3f21ea3035955859d9e1`  
		Last Modified: Fri, 17 Apr 2026 00:23:42 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e1d463ef5bb0b12b3e50fdc9de235eafd779713a97133d8caba4a58c617ac354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186629390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71661b99eb9971ee80fb204eae300bb2face7fdbfe3bfe55e67688d339809a80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:38 GMT
ARG version=26.0.0.35.2
# Fri, 17 Apr 2026 00:25:38 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:25:38 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:25:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:25:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4e3c6c4cdd578d75f743feb5d2e32e2b645ca819809780a4b471050ad09aca`  
		Last Modified: Fri, 17 Apr 2026 00:25:59 GMT  
		Size: 182.5 MB (182487496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:948cdeac9e55129253e8579bb5a59c3caa491d9118115f51ff9733181149b291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5323a336c7c5dc5709f3e9a85a6bfb7ca19cf343752e4148cebb37eff94c92`

```dockerfile
```

-	Layers:
	-	`sha256:ea48827cb3f83088b6f4aff3a319f688ebb799474f3d05d795b6c1e295253578`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 587.0 KB (587002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99ee8ea75caafbe78d7b1201518fd47a62302e0469f90f148852e978e82d67a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
