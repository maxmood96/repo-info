## `amazoncorretto:17-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:4a15f2510de3398f2434c896a5cde66d369ff81383470b3a5aee5a06b0228e89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a5513f788bc415a4c93628118f9db680af6231ff9abaac041dc6b8f596c26c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149275635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722fa6fa9b6d43de772e871f1af90c5f30f485dd98b9e424a2a3f4fcaa4397be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002f4b0a8700cfbf8303a06eadee575ca2c5115eda81e446e7e0f364c142303f`  
		Last Modified: Wed, 08 Jan 2025 18:13:27 GMT  
		Size: 145.6 MB (145649375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79a3fb48212d4552ba8f199be4bc364ad009f8891a35b694ccdbbe0bbf037895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75db8f2180aeac11e8ca329dbc87d1f1d7c077bda4c820668937c3d864ae1ca8`

```dockerfile
```

-	Layers:
	-	`sha256:4a97f218a1261c2143fa4775642084177a1bc9267b1f0c44d354bf510dbf8843`  
		Last Modified: Wed, 08 Jan 2025 18:13:25 GMT  
		Size: 378.0 KB (377973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f47aa7dd750fb2059895ebe52dc95721b86a06a0fa1d476d7af12982173f09`  
		Last Modified: Wed, 08 Jan 2025 18:13:25 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:af09574358d8680f35e7cf6c54d2db28e407f658d37a07412989a46059517b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148025487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6177232292f2f42df552ecd5cd9bc1f6cea10759ef8bee8d2837b88afe4d9ba8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29465d18296a94c04941e2979617086241bf2a9e47f8e09e5e32d73bc0d7587`  
		Last Modified: Tue, 14 Jan 2025 20:33:43 GMT  
		Size: 143.9 MB (143934718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4816b6287034dccaedbec0f92e06fa11ef081e8ef5bcfe994ede43a3d3475b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243a972b88792ff162774388c2bf9e50c4fa2827913bef0cedeaddd63eac5436`

```dockerfile
```

-	Layers:
	-	`sha256:04f19f1759c7d62ebaf8dcb75a20d2b87f3a9b5726b532d701b8b16f23e4fc66`  
		Last Modified: Wed, 08 Jan 2025 22:19:47 GMT  
		Size: 377.4 KB (377440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a82fac4b4f759971c1d71a2524cf8e407d2146c30e570f3a4eb87fc9d065aa`  
		Last Modified: Wed, 08 Jan 2025 22:19:47 GMT  
		Size: 10.9 KB (10882 bytes)  
		MIME: application/vnd.in-toto+json
