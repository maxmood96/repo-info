## `amazoncorretto:8u442-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:7976bd02b8d6dff2fc4d57007c950f7ab9111e96df68006182e858a941c2bacb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c986d92dd4c8b9910cf1d5f11b95babf929eaa7a592e08edbeeb2dd4800726c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45296693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11ce26993abdd0384af20ff8d66840be73d8a7644bbf60c14a66e77c38300e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668e33a105f8dba48db37b2326bc7788a358fe6135f8ca22d0c297688c693766`  
		Last Modified: Fri, 14 Feb 2025 23:01:31 GMT  
		Size: 41.7 MB (41654446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:23dc9b9b370845912f7da9a3a0c5fb52aac2b7af8a124bd837fb8edeb5a3648e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452c1af315e89e0edb077b8e9f8fc00ed20d3fce2a088df4dcaa2812c106e721`

```dockerfile
```

-	Layers:
	-	`sha256:6f873a107562bf333b28e2830401d33484206f4df77b7523fe197a4a0f093142`  
		Last Modified: Fri, 14 Feb 2025 22:49:48 GMT  
		Size: 187.5 KB (187487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a120025ada74964c3d346dec066e7bac4feaa2ad3ddf507f209f8c2af0b98f48`  
		Last Modified: Fri, 14 Feb 2025 22:49:48 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5834a95cddfd7bfd807c4f3235b1010bedaac2f8a97f9fce7c451ba188e9995a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45354847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7178373f705f13980fd9eba4bbf72d11419574d628c565bc2b159be038d7ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2859d01c70183d0b7ec19fcb2444ca00cf6ef55f2a82a29024c57c45b59ac2`  
		Last Modified: Tue, 04 Feb 2025 20:42:57 GMT  
		Size: 41.4 MB (41362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4c4ee09a7f484ca40f4bea6d6957c63ef810f67d136333b171085d4b14e35289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3814631252f691ad5a142c9185427c8b7616205e63c20eef3b6f4cc9f6f135b`

```dockerfile
```

-	Layers:
	-	`sha256:6aa750f9d30812489051df193b1cd3f4c6c5b7caa091f46e13480d35788c3cb7`  
		Last Modified: Fri, 14 Feb 2025 22:49:49 GMT  
		Size: 187.6 KB (187613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36a989ebb85f28937d081e47853af1f94bcb4b96ad7d6e359534817d45cd53b`  
		Last Modified: Fri, 14 Feb 2025 22:49:50 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
