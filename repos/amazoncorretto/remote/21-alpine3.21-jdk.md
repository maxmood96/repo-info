## `amazoncorretto:21-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:3b5deeb603e6d68144a736fe130c0394449d3f904230b92969559513b6b38a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b20a76bbeb736521397c211302a2260b441ea678a31861c53c8c222e92e88bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163021630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeb5df79e7e9910014f3b25059f124ab84f501a29de72c689361044eb7b2a3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=21.0.8.9.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b16dbb19cff38debb6c2e61ff99bb787ced77d851a48c4fa0e0ebdaeeec6d5`  
		Last Modified: Wed, 16 Jul 2025 21:02:23 GMT  
		Size: 159.4 MB (159384060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b38d1844c41e37c98694965cba3ed818e6c307f1c00007657006704c9f1fcdaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 KB (395904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1278479a3bd19419ff63c0f06a5bb328c6c31d9b9f84ff0743c8e89975a21`

```dockerfile
```

-	Layers:
	-	`sha256:4c4ce976ee0a74c9bfd06693e5b070074f8b686c5c9bcc5e1b61fbf8154adcce`  
		Last Modified: Wed, 16 Jul 2025 21:49:45 GMT  
		Size: 385.2 KB (385185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6dfb8498496d474154167e9f7a7932236ad82ffe91a2fd9c96f1401032a58f8`  
		Last Modified: Wed, 16 Jul 2025 21:49:46 GMT  
		Size: 10.7 KB (10719 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5953975472506d2a4e82198fe3b15dcfb119efff7ebf9538796cf374eb962a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161328507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a60289eff132940b11c225a1c59501dfefa373c2dbdcf39762dfca08a17d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=21.0.8.9.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25112af747a898d03343feff94f9277ab488fb24970fba3118bc70a4628d5e11`  
		Last Modified: Thu, 17 Jul 2025 03:51:24 GMT  
		Size: 157.3 MB (157341570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b046b2a235f9fdd66ea0364f3d4828f3b3c6e342f9828b03a30a1891adb8882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.5 KB (395524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d331637f8e3954b1f6d3948c82568c15e665472408cd3b44bbecf9c474715b6`

```dockerfile
```

-	Layers:
	-	`sha256:3b66b360ed31b16b21a64fe8031988c0647403825c500514825ec252318a8c43`  
		Last Modified: Thu, 17 Jul 2025 03:49:35 GMT  
		Size: 384.7 KB (384652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38150ab198d0784508c5f4d9f529e3ae53cc0fe949db431d04780693627c995f`  
		Last Modified: Thu, 17 Jul 2025 03:49:36 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
