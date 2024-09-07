## `amazoncorretto:21-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:fcced7f79cd16703a7424af871a3065884f98abd5972f2d2f3db7b5c208ef736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ba9fd2512269da18e93300445b8a886de18db5a69324e98bbff71a49a140fa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163142110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfd4b6be9d49b156643c7ca751dac5ebfec75f8fa8bbf6fe935178d8020a024`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d6545d19a7b077258bd4a10655f634388138cf7fb60343e126eafa3365fce8`  
		Last Modified: Fri, 06 Sep 2024 23:17:52 GMT  
		Size: 159.7 MB (159725797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6edec41c497436fdeb329aae6cbabd065d17cd7680555c1a705fe9fdb3d8971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7705bbc2fcf0e989fb2ee7d6064ced23d68464e546452606224cd5e3c284857c`

```dockerfile
```

-	Layers:
	-	`sha256:1f6979721e5ec497722e1b4955e56a94a6c7dd8fc1599f8a4b30fe541f864a00`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 380.7 KB (380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b28fb468294f925075c7f435704e286a66512f99fd432e30a5d8463511fc68`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:03287f5c016693c34c88fa7a8a7ebf7c469006fbedb02739d782439e92bc1c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160822030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1170eda4627b90f41e1189d3fcb8c50ce389bd9f9d30e18a7b4582b0144c7827`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ed64278a86a3c40ea15ebf95a8a280fb4550bc00beffce43db2aa8b42c803`  
		Last Modified: Sat, 07 Sep 2024 12:14:13 GMT  
		Size: 157.5 MB (157481683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:50026b6463613e4aacc347421b2131cc26e75f436198717889d679306afed88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ebf1113dddc912a13c7e7d30930e52089e60eaf8e42cd0def75cefff7ba0d`

```dockerfile
```

-	Layers:
	-	`sha256:09aefef29f8806ef0c945ee11fd1d21af21de784414ff77b1e863d74f1a74c95`  
		Last Modified: Sat, 07 Sep 2024 12:14:09 GMT  
		Size: 380.1 KB (380071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6a9a01d413b469f3fb556e8c7e3387ef6ac837c7eb32b3d442d12a284aba56`  
		Last Modified: Sat, 07 Sep 2024 12:14:09 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
