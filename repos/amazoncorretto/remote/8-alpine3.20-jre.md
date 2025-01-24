## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:8d4c88435126dc34c370c47007483038082486317b721a97c60a1693ca8ab8b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b015ee2174fcd47131a123b43ed15b2bfa3c7c7ca1d3dbf3487571ad16d06efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45281050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece9bc4c47584a92efe3d50e9fddd38feb1b75709548a91dfd847259bc592a26`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f3be42c6b613c990c1a8ae9a31b50e0be2641c31d05632a0d30da928fe8b3d`  
		Last Modified: Thu, 23 Jan 2025 18:27:08 GMT  
		Size: 41.7 MB (41654790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de1c1d50c2f5153eacaee0883ef4ef236d8d2e5fc49091fdd45cf2c945f680a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bee491f6bae9829cb182889e51975323ecef1a90c50bd4cb31b1ea224ca390`

```dockerfile
```

-	Layers:
	-	`sha256:e15e694535a2eae7b3f6ad98d6d38caa42e1f1c8344892f78fe8aef5e8c6d413`  
		Last Modified: Thu, 23 Jan 2025 18:27:07 GMT  
		Size: 181.8 KB (181761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb1d43ac9b45b107cb28fda0b721b40905dd847506667a08878d53e4b061fe5`  
		Last Modified: Thu, 23 Jan 2025 18:27:06 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18ae64b5351f6fae270c125dc1f76b4c289611faf39ba1f792d1789cf050f6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45452431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4263d88317d16358040d25679848d1fdd044a0c25158b9f55453a3ab20f66026`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf9547a77b88c3902f8a2af9e7814ceee0eeec6cf040542530ebba8f58c976`  
		Last Modified: Thu, 23 Jan 2025 18:33:57 GMT  
		Size: 41.4 MB (41361662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e49f1959fa3a13b1903016a2a048448cb9129487712128366a0515544c8e857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9c70630f2dbeca5b08b371729f7f072da501527163b48ea877c35deaaf284e`

```dockerfile
```

-	Layers:
	-	`sha256:cc11f3f5321c6b6aae136c47a8a38f11a96875154974eb23374d28814bee1a9a`  
		Last Modified: Thu, 23 Jan 2025 18:33:56 GMT  
		Size: 181.9 KB (181893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23e219dc4c7835ed6ace1fba70783496cb2b289cdba0ec2bd4598e048e167cc`  
		Last Modified: Thu, 23 Jan 2025 18:33:56 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
