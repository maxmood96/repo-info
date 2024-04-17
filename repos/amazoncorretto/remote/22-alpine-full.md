## `amazoncorretto:22-alpine-full`

```console
$ docker pull amazoncorretto@sha256:c7620042a87ace5c5726dbc5da2bf76551c9edb2371cd7983bec9b5df250e157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eb732edbc33f3870729c0d8c5b1255e10d3962e5dcf4c3308805ec9bbfc2aaa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161493083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e41f3b88e0afc11e40176d8795a65cd9cce396628c096603e5afa3b5e116a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 17 Apr 2024 00:08:27 GMT
ARG version=22.0.1.8.1
# Wed, 17 Apr 2024 00:08:33 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Wed, 17 Apr 2024 00:08:34 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Apr 2024 00:08:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a771612d132ee22cf7232c90161c570250ebdb4ed22f528c387513fc1218921a`  
		Last Modified: Wed, 17 Apr 2024 00:29:39 GMT  
		Size: 158.1 MB (158084354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e99669c9aa83d473171b4d902d4f509e97258611568c0426c00ad716c170433
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158782468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112f862aed8468b6833c28e9ecfb6858c10ec2c43afff64e6a13bcff37152400`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Apr 2024 00:17:13 GMT
ARG version=22.0.1.8.1
# Wed, 17 Apr 2024 00:17:17 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Wed, 17 Apr 2024 00:17:19 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:17:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Apr 2024 00:17:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85dc265b18adf7a5dea1a9a4e69935e312d8d88fddd2378466dbd6bea4bd15`  
		Last Modified: Wed, 17 Apr 2024 00:38:19 GMT  
		Size: 155.4 MB (155434753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
