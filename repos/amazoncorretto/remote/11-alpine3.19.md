## `amazoncorretto:11-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:5b5054965ac2c8966462d3553b5ff284fbd7a7ee67e9139d17d97ade4a8b0fd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6dbd515b7bfc76df2a2d7a8ff31868af9a91bec61c4c497cde40a2b4ae424a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146924899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a096537407401877e32b1324bc29948803227c4f87dc662b8398b5223cb6788f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d121048351ac5a66295d3b230e1c80830ce5484eb8c3c0c278b50abbf8df8dfe`  
		Last Modified: Wed, 22 Oct 2025 01:07:58 GMT  
		Size: 143.5 MB (143505084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:598457899d8c3ea530e1a9f10a7698085762d1ddd0cd0cc2b2d817347d899862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 KB (601272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456ac60288d03fad547d1766b3adfc84b8f16bf9ee4ceefcd3910b29081e955b`

```dockerfile
```

-	Layers:
	-	`sha256:2aec810d47764b78b8c24b10452c9bad553d8fcf6a21a58668d7c3172ec81a3d`  
		Last Modified: Wed, 22 Oct 2025 00:48:17 GMT  
		Size: 591.9 KB (591856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f3c65022c3ac2ea05bcd0baec3dea49aa098443c4f20e2e72ae7088494307b`  
		Last Modified: Wed, 22 Oct 2025 00:48:18 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d1265258f53669cad17ab82a323cd6b1e44f7160b017305ff75f1bf8076283f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145150588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dfa3f7d2d7fb83cc41a9a434a3b9efeb5b60149d2deb14365f6eb1df08168c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f2f88c2ecb4fcebc9ca654aae7b7b660bf2a3df22892b73d3889d62803a800`  
		Last Modified: Wed, 22 Oct 2025 01:08:30 GMT  
		Size: 141.8 MB (141791287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:99e43709289db43e3d4d67829051b9eef56e8f0b3f6c874ee40567e0fe00e561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 KB (601433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157fd80830d3e5250209c900ca8d4dfdac7674f4e8e9f3ed472ebdd2cf09e238`

```dockerfile
```

-	Layers:
	-	`sha256:5cdc9c1d80bea12d33ddd25877dda8085e95f7756cec4f862c5aa5bbf34133ad`  
		Last Modified: Wed, 22 Oct 2025 00:48:21 GMT  
		Size: 591.9 KB (591912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58062aaece8bd00f8fe45fa1994525daf410eff9f260e169becc9c779f7a359`  
		Last Modified: Wed, 22 Oct 2025 00:48:22 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
