## `amazoncorretto:21-alpine-full`

```console
$ docker pull amazoncorretto@sha256:cc4c1d0cab18894f4470b3afda995fbda8b5166d9d646205a18357b2b20c4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:02248922f536b975c5f1fc00c36e6bebfb4bae5b95eaf77f034251b47abd3954
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163179131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d13de5830cae6c573635c5ab506b565b4808af683d79f4aef6d43252f2382a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 20:55:13 GMT
ARG version=21.0.2.14.1
# Tue, 27 Feb 2024 20:55:19 GMT
# ARGS: version=21.0.2.14.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Tue, 27 Feb 2024 20:55:19 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 20:55:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 27 Feb 2024 20:55:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4589e6e5da0d67f804c83e55296c9d83cdb9e91368a23fc1645ab702d2fdca1`  
		Last Modified: Tue, 27 Feb 2024 21:00:15 GMT  
		Size: 159.8 MB (159770402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e42a28603fc2b98f4978e4e600577c637a3f51f89f7e21c052ad12b73b879383
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160689960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4b4670a0adab765bc35e23110c989534edf1350c35e22c11b5e5a08c2fec8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 21:09:32 GMT
ARG version=21.0.2.14.1
# Tue, 27 Feb 2024 21:09:38 GMT
# ARGS: version=21.0.2.14.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Tue, 27 Feb 2024 21:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 21:09:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 27 Feb 2024 21:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25357840a908bb2912a76568c2ae957a450d2aa007eabb22be02e9a54039fd38`  
		Last Modified: Tue, 27 Feb 2024 21:14:41 GMT  
		Size: 157.3 MB (157342245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
