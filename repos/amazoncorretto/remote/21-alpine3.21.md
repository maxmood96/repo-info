## `amazoncorretto:21-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:6947a4f635a0300d83ad270277b6b719cb3c1d1d9f348d5b991f83826a1c2d42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c69fc04790deb78f4c123862a2a2956496156e4679636bb4c78c8294de18dac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fdebd8f4397e59106ca57643ed8f63ecfed2dfa41e97b6f307bb3acfcfd755`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:06:49 GMT
ARG version=21.0.9.11.1
# Wed, 05 Nov 2025 01:06:49 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:06:49 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:06:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4b7b858285881f41ae4743302dc81974bff641d7cf71eebf1552e34c31da1c`  
		Last Modified: Wed, 05 Nov 2025 01:07:08 GMT  
		Size: 161.6 MB (161559896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2dde3f8e792d262ec46c0dd36cb643867e22c5e9261ae8f7d1e76dbaf3d52e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 KB (595829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fb64c6a164de0d1f1a03f3405719fa7336c7cff69151afd2a29af39c2e6212`

```dockerfile
```

-	Layers:
	-	`sha256:37ab56672f76d6eeba493ee691d815aec06d4cbe289208bd09b70fa8126480cb`  
		Last Modified: Wed, 05 Nov 2025 01:07:03 GMT  
		Size: 586.5 KB (586458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4bbdd3e9fa2f110a83d220a54d17223f5422b41d301fd3c739eaa3251da148f`  
		Last Modified: Mon, 05 Jan 2026 02:18:31 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fce4ecb4d28ebe2c930232704f83933a05730dd692017e1cec84ca6a11973d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee6dec2fd00a35af546e4074007ed66e21c6a2e9eeb5a414cdbd72a535deb15`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:20 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:20 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3a14b59a66bd18cc414432756e3cf15f091bd7d40e951dabc60b97aa88fc6`  
		Last Modified: Sun, 04 Jan 2026 06:06:07 GMT  
		Size: 159.6 MB (159581794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f3bf3b5ed72fc933f84ee7b98105ad248d4e163c70740a8461661df80a2f71c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 KB (595352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841b9c1236d76fa273070de7ce0dc5b5df7520ccb5afffe89f755c5bc52ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:39f0dab4f3c01d96dec796bf70c51c14fb4e219d748fe2364dd2c8a18a87be62`  
		Last Modified: Tue, 04 Nov 2025 23:16:37 GMT  
		Size: 585.9 KB (585877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9ac3959ad64f9e80a00a972351d2a4b5294dcffc29042a992d54fec441a814`  
		Last Modified: Tue, 04 Nov 2025 23:16:37 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
