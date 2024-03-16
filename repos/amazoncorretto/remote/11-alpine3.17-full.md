## `amazoncorretto:11-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:127fe6eb292b5d11f9f5a1db3c71032e8f3fde2d9b4119ce63fcf3e90734d442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:edfb6968ad79a3ade9b845c3471a0e1800c92a625029b0ecd46afe6db2df8ae1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145055440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce34047985c37b75c53f2c424047266552ee6217530f7218ee572a76ec6d789`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:52:16 GMT
ARG version=11.0.22.7.1
# Sat, 16 Mar 2024 02:52:22 GMT
# ARGS: version=11.0.22.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Sat, 16 Mar 2024 02:52:23 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:52:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 16 Mar 2024 02:52:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6b61831c72428913ac77490d6047f1db34304757f9719c7d5a6f649f260ca8`  
		Last Modified: Sat, 16 Mar 2024 03:09:04 GMT  
		Size: 141.7 MB (141676036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3312046cdfd823e204fa44f78c5ef2e9d66ce9d0580ef3da2c52ddea4d2964f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143014910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ebf262f8343f4b25b0acd69392c1e71c8edd7005b332bc50ca1d96aea81c5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:42:09 GMT
ARG version=11.0.22.7.1
# Sat, 16 Mar 2024 03:42:15 GMT
# ARGS: version=11.0.22.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Sat, 16 Mar 2024 03:42:17 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:42:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 16 Mar 2024 03:42:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425749b8bef87fdab9a8ac8e12e5c2221860a842df01f39006aaeb63804a1f27`  
		Last Modified: Sat, 16 Mar 2024 03:55:43 GMT  
		Size: 139.8 MB (139756627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
