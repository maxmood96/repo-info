## `amazoncorretto:8u442-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:4a2d1496836322f48abbc4e8347d0dc5399e87ae80f035254c7f8c782a7204ca
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
$ docker pull amazoncorretto@sha256:604ef063484c0f9e9a612e0d793edaa838012d026f86fcf0a13016aa1ed52dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45355580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f70618bd3e8ca375ce3235c22c15de9a27bc0db33cd62c82687edb401b4453d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61661762fb77358fdc657118e68ceb39b9f46761ce4c9d7dd0436754b64d43c0`  
		Last Modified: Sat, 15 Feb 2025 12:13:11 GMT  
		Size: 41.4 MB (41362551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47552607972d68f734bc954a02208ea2df1c76c7fc916473d4e557f3d0d27912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7752d7d748b22d1745126644a0a78930b94e461997959eef2a92ac87df6ed165`

```dockerfile
```

-	Layers:
	-	`sha256:8d004110c45c1f580e9c5c201be223d1cb2f1f4a97744575dc2dbff2f4e0d917`  
		Last Modified: Sat, 15 Feb 2025 13:48:28 GMT  
		Size: 187.6 KB (187619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7eba2c51e16fcf28a7399b7bd526ce009a0ba4c24284062a862d7c52c0143f`  
		Last Modified: Sat, 15 Feb 2025 13:48:28 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
