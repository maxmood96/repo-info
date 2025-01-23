## `amazoncorretto:8u442-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:9b23d9d64b3c1ec8111569c97e4a0962d3ead889effdc58bcf359edf73a73dcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

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
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf9547a77b88c3902f8a2af9e7814ceee0eeec6cf040542530ebba8f58c976`  
		Last Modified: Thu, 23 Jan 2025 18:33:57 GMT  
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
		Last Modified: Thu, 23 Jan 2025 18:33:56 GMT  
		Size: 181.9 KB (181893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23e219dc4c7835ed6ace1fba70783496cb2b289cdba0ec2bd4598e048e167cc`  
		Last Modified: Thu, 23 Jan 2025 18:33:56 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
