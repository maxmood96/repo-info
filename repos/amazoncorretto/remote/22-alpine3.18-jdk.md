## `amazoncorretto:22-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:10285aeef26f926a2fe04899355e1c6f2572fd766fa1a4ef3496a38a21df127f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9defb67b87be1d8ff6f3431e314eadc0c6711b4502545b3c571abe0bcd6dd56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161012386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b5c3391c83d4ee4fe959308e0f19ab01f60e68d11da0d0d7e2d4ba82f59583`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:97c11cbbe0740aebb775cf530da403faca20ac225bf10d49ea761b3ceedf15a8`  
		Last Modified: Fri, 06 Sep 2024 23:18:11 GMT  
		Size: 157.6 MB (157596073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6773fde12d0e1eca0aeafdf66501b98d906a3ed083cd35a96309591bfab4ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6556f7b890c7b24f4f589273a621dee77b8d7b3ad59c33d2e99c173337d9ff05`

```dockerfile
```

-	Layers:
	-	`sha256:226f85f73528df84399356fcdcd49450c4f1fb9d1b2b974913e08fc7ab948303`  
		Last Modified: Fri, 06 Sep 2024 23:18:07 GMT  
		Size: 381.2 KB (381246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36769d20d5c9c728cd747075594057db3f07c75b591c5fa4d00b4c1f9d76e3c6`  
		Last Modified: Fri, 06 Sep 2024 23:18:07 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a5751af93cb144fd8e49b828eab0fe3d620a296729f88a9d6285fbf443c84ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158534206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71bb8b56bd393ed299b24f4cf6915c91ab4713d52c19473c65470d01cd6bac1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24caf9c515c953c92c2982a6c284b78d53e56054cde93c88fde8ee390fe9fd70`  
		Last Modified: Wed, 24 Jul 2024 10:47:32 GMT  
		Size: 155.2 MB (155194712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:65b925cd044207a4a6b0c9e6320acb562aea785acc9917285cf6c21f5937b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cf4a59211c7a9624ce955760e04b3ea2b758258bf755afabf9bab559fce575`

```dockerfile
```

-	Layers:
	-	`sha256:97fa1e71cc31ea846bdaca09b38183dfe0c30eacdc9e34a18052054564981a36`  
		Last Modified: Wed, 24 Jul 2024 10:47:29 GMT  
		Size: 380.0 KB (380023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5f75a1081d6de7178bf721d9f89e18d5ff77f580791380c4e5fcad2177f65c`  
		Last Modified: Wed, 24 Jul 2024 10:47:28 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
