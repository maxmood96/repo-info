## `amazoncorretto:17-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:e382a8e3d05078cc1925e368b5333332e3181519d4282de82d0f605a78d6fb83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6e497502393ff1cb50a7bc0a09c85fe9335393f396441cea55e55669adae91b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152394363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1147928176b06843c10d22860fa9377a260e89aa5c6180050eabfb892cc9d34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:23 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:23 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:23 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a5d5f25598d7d31e5def8ddd22565544849b478a57a5a13c81472e5fbd099`  
		Last Modified: Wed, 22 Apr 2026 21:34:42 GMT  
		Size: 148.6 MB (148586174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b63d4b0ab1686da9cfe04ed19f2573e93ef9ea02d04babb598bc33a651511dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.2 KB (593161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4b9caddde2a99396a497e8b29ac42be0e60d845c3edc25e6a5ad3f75afa2fa`

```dockerfile
```

-	Layers:
	-	`sha256:e5bac6b2bad559f83e93daaf015cb3964b0e879c08542b0e25ce232c86c81d4d`  
		Last Modified: Wed, 22 Apr 2026 21:34:38 GMT  
		Size: 583.8 KB (583782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9cb683ac7841c647a99e14306d6145c46fc6cbc56d58055c22dd873ebd6e3f7`  
		Last Modified: Wed, 22 Apr 2026 21:34:38 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9b047d13d621ace8c51476b95ee03466923d0c430a3bd4b759ea1171455bcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151077423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dc5ba41c7be4392376932c66a05979910e9cfcf3703d9b07852a5ee99da0d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:10 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:10 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:10 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfbb9c008e48cd8b7740b1bcbf1b92f4b0a9d2d6d8e7450b4de9f3a734ba99c`  
		Last Modified: Wed, 22 Apr 2026 21:34:28 GMT  
		Size: 146.9 MB (146935529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:83ba52fd04b3314989cc4b9c0d1a3ed3b78859115d1f06ae843ca0305b248aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 KB (592684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b7af6d1c6660cf8f3942d74e1a753c3208102a0692be5af336b8dc2ea0d29f`

```dockerfile
```

-	Layers:
	-	`sha256:d75e4a60ed559601bbd984b29c8f038066b2b49eea91e6570286566ca719a29b`  
		Last Modified: Wed, 22 Apr 2026 21:34:25 GMT  
		Size: 583.2 KB (583201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e020de182b5722b1281646d8d684ead4a6b82af30ad22419972f69ee75c55df4`  
		Last Modified: Wed, 22 Apr 2026 21:34:24 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
