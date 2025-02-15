## `amazoncorretto:8u442-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:d3a844afab9b3584f0fed811b2dbfc8d2c08df562228da0ca97002b98bce48ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:10764fc9a585700ff5dbd5c03eb10d9167e3350b97c47ab2b93f3430ddb8bcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45281710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2a875349cccd08f2b7cceca1975a0c22efb46234c553661167e460b1ab2be7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe3316568af26ceca7b8a13f1b5f5038c90fa62e92da452377d1a2a81a3cc0`  
		Last Modified: Fri, 14 Feb 2025 19:12:27 GMT  
		Size: 41.7 MB (41654813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df8f69b6171c491c63898e9b0fbd77846d6146bcd49b7db55f9487d944dfe320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 KB (189799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae0976de134f216abff0fe729c27f607feb98495d66fb35696a6f32af0a1158`

```dockerfile
```

-	Layers:
	-	`sha256:3d0a4644b30100f929fc5029bf6bf559b03d3ce53f7bbacf327846e30b36b7f2`  
		Last Modified: Fri, 14 Feb 2025 22:50:11 GMT  
		Size: 181.1 KB (181101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46a26e8f04c2f18451ff5f1be61202692824cd163e70da5e8a716465a152d185`  
		Last Modified: Fri, 14 Feb 2025 22:50:11 GMT  
		Size: 8.7 KB (8698 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-alpine3.20-jre` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf9547a77b88c3902f8a2af9e7814ceee0eeec6cf040542530ebba8f58c976`  
		Last Modified: Wed, 05 Feb 2025 11:40:19 GMT  
		Size: 41.4 MB (41361662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.20-jre` - unknown; unknown

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
		Last Modified: Fri, 14 Feb 2025 22:50:13 GMT  
		Size: 181.9 KB (181893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23e219dc4c7835ed6ace1fba70783496cb2b289cdba0ec2bd4598e048e167cc`  
		Last Modified: Fri, 14 Feb 2025 22:50:13 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
