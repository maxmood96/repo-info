## `amazoncorretto:11-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:84f21946e9f1981e4979f39e7d82842ad7ce13d93969e43a2592a0e4581371ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b03c49392b0ebbbd31f6d270cc184086ea3f9ad2ac6878c729c645c156cd2911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145532405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918d7a5eb700b6b0cbe6956a83bc23e8e0857ef363d8bd373221581c86ad41e5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e37f65f08727562421b90179a5bc71a9db33e28fb6e68c95b4a998e1643d76f`  
		Last Modified: Wed, 16 Oct 2024 17:56:12 GMT  
		Size: 141.9 MB (141908598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:00ace3fb0f9f5362c0e4141ae2c002a45a1600a23320719771baf0fd5f38b877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 KB (395828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06783c63b9a1540fe8c43fbaba127960e9711975282e91be14d283e1fef12141`

```dockerfile
```

-	Layers:
	-	`sha256:0afa264814d13463ef4a8fb0092070a11817822445ee21f4e3b5640f70ac5e33`  
		Last Modified: Wed, 16 Oct 2024 17:56:10 GMT  
		Size: 385.3 KB (385310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bddcb36ef79502f520cd396ec73aa2b5e6248a57f6c97c59d42bf871209f555`  
		Last Modified: Wed, 16 Oct 2024 17:56:10 GMT  
		Size: 10.5 KB (10518 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a8cea4011a2910ebaf1314205f156eaccac0778450e9f28d00aab7d13fbd13b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144118437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07827b80c9b53644fd5e6948185d134a6e391a4533002c411c250b7a17ee82c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d75e0b84f6a291f6a433e35e083f59f3d0af9f4e372a4ba452f6ad81e4ab3e`  
		Last Modified: Wed, 16 Oct 2024 18:19:12 GMT  
		Size: 140.0 MB (140030791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:99a4afebd171e3b72e55cf6ee7b27081a8b30bcb9cce9aae2df6e470af624fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 KB (396078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddc02b826f93b211dc7dabe3c6b5349a5b624f1c4f450765936f60f4fee3d4`

```dockerfile
```

-	Layers:
	-	`sha256:25951ec21b652e22c3bb191b1c55db3ce20f435fe65c2b7ea9c3f6cbb8966b07`  
		Last Modified: Wed, 16 Oct 2024 18:19:08 GMT  
		Size: 385.4 KB (385414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a209a7c402a13f05b564456bdcb1669c82f6f2ff1282ed6c6e6dccff3bee6c`  
		Last Modified: Wed, 16 Oct 2024 18:19:08 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.in-toto+json
