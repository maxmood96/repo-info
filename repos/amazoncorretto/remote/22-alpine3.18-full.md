## `amazoncorretto:22-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:e87868ededfa853ac184829ea400035696bc9fa3d9394e876609be0505d1ac21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.18-full` - linux; amd64

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

### `amazoncorretto:22-alpine3.18-full` - unknown; unknown

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

### `amazoncorretto:22-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9eb0b9dc85cd35ea87e132431ad63d8d1931ae063f25d67042b41a92f5cfd062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158534891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45681d69d459f4c800beb70aa88947207decb508545a2e5e768ec88718d2fe79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a4c4c59c8e8c4aa02e8e7070fbc450e4f25b508ff43fc7ffc915d16e303079`  
		Last Modified: Sat, 07 Sep 2024 12:16:47 GMT  
		Size: 155.2 MB (155194544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:80d57bb191640949c41bf276d17e5509aa8f350168d48659664b334ec0b8ba1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca60aa47ae3fc4993b16ca250b72a8f2ef82b8ce305fac55eed84f50350c540`

```dockerfile
```

-	Layers:
	-	`sha256:11ce17734b822137279d6321c68a97c4beae86a40aed491e6e64b31da5626514`  
		Last Modified: Sat, 07 Sep 2024 12:16:43 GMT  
		Size: 380.0 KB (380023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a87f028551638e21f2815ed5fa7dc3b53a512f762d811f1e70b5c1c47b0e212`  
		Last Modified: Sat, 07 Sep 2024 12:16:43 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
