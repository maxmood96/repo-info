## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:a8f6f7770a6dfae02f483b97a318c8004b4f958133516790da6d218bc6ba8a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4878618fc1f260591dfcd6abee725a755ff091fb759c7a1e4c41df55aa0072d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149099379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba86f56dedb824be5e49e1a42e16d59cbb3d4a6b92ce011a122749ae25ca623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673a50245414758c8b1639205b356156de8130b62c6e8a96f49502ada12772ad`  
		Last Modified: Fri, 14 Feb 2025 22:55:55 GMT  
		Size: 145.7 MB (145678511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8633b0a184377f1a86ec971efda19ac0ac0959837c4b2c558ad71dc7d52fd174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32918256453c94e69b426143e88369a22359739781c25de9ee964b691f1eabd`

```dockerfile
```

-	Layers:
	-	`sha256:31c432473781c8b39ec67fef4b9599077b1f015518d2dfe6d31e5df91ef59770`  
		Last Modified: Fri, 14 Feb 2025 22:48:09 GMT  
		Size: 380.9 KB (380893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c1f9cf179589adce6c56c01e54e40d0e350894164ab18e908f65d02a51a7d3`  
		Last Modified: Fri, 14 Feb 2025 22:48:09 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27977af4513edf641a7d549e976a73aafabe032a9068680c92daa775d165cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9672a44fb8e730c7cc500e8dd28e2c31823d37784c49065c61206e0d92157ed9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4764cc5cfceb8f11be8768feb456ba10642f2ef3caef7921575286ca20551ef3`  
		Last Modified: Wed, 05 Feb 2025 09:22:42 GMT  
		Size: 144.0 MB (144021854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f94ca04c8f585fe6ecaf5fe4a6c7c27672739d2277fdcadf6e4eddf9986bbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71896a2fcce59365e5804c471d55549dbc7746bd620ad1f7add84cca30af4301`

```dockerfile
```

-	Layers:
	-	`sha256:4639c8de075d975362c9ef467312ab1add84d7ac7e5d885951a8f4140029228e`  
		Last Modified: Fri, 14 Feb 2025 22:48:11 GMT  
		Size: 380.3 KB (380312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a85ae0245d32402bebbc106f2e3b129c176f8b94c8b5ed93ea33767a43677b2`  
		Last Modified: Fri, 14 Feb 2025 22:48:11 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
