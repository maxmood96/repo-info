## `amazoncorretto:8-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:a6d6f85e511e19a371db844a1f22a1baa39420428fb9321b49abf0d6e1b98b68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e4fa17110d82dfc95e4a5bc8c49a5ca37efda6af79de6c46c974cdcadaa1595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103540094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c614a9aa4c39e645e33c4ea59bace64eb02c5c8f4f57319b5522cf4da9afe6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:57eebac4290f3e8e977d83a9f3378054fb74142f1209a9bbca0a46098b203ab2`  
		Last Modified: Fri, 06 Sep 2024 23:25:53 GMT  
		Size: 100.1 MB (100123781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:284b9cbe487d0b209cceba02aa5a25d4aab86a7171f8a04fb2c9ae324bcf1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da3a59ac3db71ee343b51d2337159411adfe9420e5ddca6d699955da41b65a1`

```dockerfile
```

-	Layers:
	-	`sha256:a99874cd4067727db40873e5ec5b581abe408c437600e93cea80cd9b9a187813`  
		Last Modified: Fri, 06 Sep 2024 23:25:52 GMT  
		Size: 245.1 KB (245075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a704684a60befe1d5133933ee3a942cb49aa7884b488c7e66df4fb58b3e430`  
		Last Modified: Fri, 06 Sep 2024 23:25:51 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:37304060f83f2c6736e3e27ef87ef2b9fa8972f2aa739891b3355ee6fdbb3829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103176356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5838c2a15a2ad272de4f8d0dd376999946d9d98e5d3d87c0e39c0000596b815`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:b2b561c57794c194cd4e9d42af6125df0ce514e92517d6b567513e958ca621e2`  
		Last Modified: Sat, 07 Sep 2024 12:06:01 GMT  
		Size: 99.8 MB (99836009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6aab5be0b2724842bea23a5784a8f8c2536529d5384cc18e651a18f5ca403a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 KB (254658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2005695d3280fab37ec82ab5e44c7c0db3deefee8fae4b407f22a60398dbb801`

```dockerfile
```

-	Layers:
	-	`sha256:d6f4221660de744130d12acb024881a87b3fd4304fb7d75eead2f97e657bb66d`  
		Last Modified: Sat, 07 Sep 2024 12:05:57 GMT  
		Size: 245.2 KB (245207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e79f9c9faa9c2ecc31a0c1baabb329695e150d714f74f5384e0526d0097a28`  
		Last Modified: Sat, 07 Sep 2024 12:05:57 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.in-toto+json
