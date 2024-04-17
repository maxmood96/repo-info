## `amazoncorretto:22-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:acc62935ea597f947f4fb4676edc551b44c8193e8ccd78d1734d4d69ce467499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1cf8c776b0e1f8e1177e46fc9d1a125ec946fd781d6a07745f4a880588db2ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161463801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ae5abea8364df3d4310e6a9ae225a5f2bff3aa5a842c366ccb0df63699543c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Wed, 17 Apr 2024 00:08:04 GMT
ARG version=22.0.1.8.1
# Wed, 17 Apr 2024 00:08:12 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Wed, 17 Apr 2024 00:08:13 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:08:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Apr 2024 00:08:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec91851ce2aa4671fff8589e021830a5081007152595ec1f108cbce714dc691`  
		Last Modified: Wed, 17 Apr 2024 00:28:47 GMT  
		Size: 158.1 MB (158084397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4f41bb7843d6e4808bcb3329cc34ed3c28278075f2762b87061a79834b232d2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158693011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6d02f2abbbbe866875debe2e71d828fe99f38838d13f7accf2250d39867146`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Wed, 17 Apr 2024 00:16:53 GMT
ARG version=22.0.1.8.1
# Wed, 17 Apr 2024 00:16:58 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Wed, 17 Apr 2024 00:17:00 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:17:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Apr 2024 00:17:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f7a5ca99e1b09889589993cb16223e971277bf8a6baa687a889c904061570`  
		Last Modified: Wed, 17 Apr 2024 00:37:33 GMT  
		Size: 155.4 MB (155434728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
