## `amazoncorretto:25-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:d6e0c2a65bae915aa968727f81e912c1b8d74f232de2e3b44a409201222f3ca5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ec6dfe72d9906276d77ac45ab8c099100aa3e437022f54dac722cb7ed1041f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184399007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973e0cbb0301afb4fe6c5a735b8251788c12e5e62dc41c4fd5a7205d44d72d96`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:39 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:01:39 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c9faf3caec023660401b05f7ccd941ecf0e4ec27a18d879b81a3dda914e200`  
		Last Modified: Wed, 21 Jan 2026 19:01:59 GMT  
		Size: 180.8 MB (180756438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d410ab353e5f6a65ec974cf8761387a5f40d9ce20e03c0bfccaa79751b8f8ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 KB (604932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4dd1b9eca8aeffde7a40bb8daab99a578c9b3e31b1568bfab1da7072b0f6d6`

```dockerfile
```

-	Layers:
	-	`sha256:6d6116407ce707ca73eab2421617ad12de7ea5e54140b042246ad85dee291458`  
		Last Modified: Wed, 21 Jan 2026 19:01:55 GMT  
		Size: 595.6 KB (595560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bfc61b3f5b420dfd783a3a6b4e0e21db3056b9585259b2a06abcda7cdf75036`  
		Last Modified: Wed, 21 Jan 2026 19:01:55 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e10c4c0eee8a5684306e7d8181be28f52c6e993e82059c3eeaaf27fcfccf716d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182395350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99b2cc82f0bc5a4c7c638d79d0b3bcb2ffdbb912f0f8d6f8d15dbcfaaf4d1f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:02:01 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:02:01 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:02:01 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:02:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d1f6108496158a1c82867bb59ddc21b110414d1d9b3927664fa5319f0f5591`  
		Last Modified: Wed, 21 Jan 2026 19:02:22 GMT  
		Size: 178.4 MB (178402997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c77748a6947498f68f06747bfe2db98fb051f91a2ea0dc4c2c67be84fdc3ee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.5 KB (604452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051689f8eb00d608743b3b26b037af49b708779c199be68e7e9839b7c84e7205`

```dockerfile
```

-	Layers:
	-	`sha256:26fbc145985a371c932e77c9cc0e0544a0eb6f83610217a2dbedb9ef6021809a`  
		Last Modified: Wed, 21 Jan 2026 19:53:57 GMT  
		Size: 595.0 KB (594976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59636fc76cd87562ab249ee0f2abe6dabb31b67e679eff8a0759ed7c1e7ce8f9`  
		Last Modified: Wed, 21 Jan 2026 19:54:05 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
