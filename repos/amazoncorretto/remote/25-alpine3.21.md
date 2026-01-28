## `amazoncorretto:25-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:3ccab3df641eafeeb056d20bb23a618781d820ec173184ce490fbcb0386cd5a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1690d4eea977791c88310c69e08305cd2c1a28023a40e6a6ead0a25c05ffc5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184400205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46eb8055ae6841a6ef321ac9a9bb390722b00d34485cd29828e7a8366bcd5a8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:51:41 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:51:41 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:51:41 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:51:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:51:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8a62d0aac35f47d1c0c27f2e706f21c5f21b96248a15399a7843e0a07d237`  
		Last Modified: Wed, 28 Jan 2026 02:52:02 GMT  
		Size: 180.8 MB (180756463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ee56af8dd197f46d3825e0cba955fa0baa1e7fec68374623a70e1796ac7502ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 KB (604932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e67f6412316003c95c6a0cb8cdf50e37bd6e4ba6deb8507daa77788164fd3a`

```dockerfile
```

-	Layers:
	-	`sha256:ff723d10992c30cd45a7dddfc20f7dcb5a0bf237e7f1261b9c177e9e02f223ea`  
		Last Modified: Wed, 28 Jan 2026 02:51:58 GMT  
		Size: 595.6 KB (595560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc677667b14347e82415afd32ce517e3a920592d378b530b3ee118f955f07434`  
		Last Modified: Wed, 28 Jan 2026 02:51:58 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
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
		Last Modified: Wed, 21 Jan 2026 19:02:18 GMT  
		Size: 595.0 KB (594976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59636fc76cd87562ab249ee0f2abe6dabb31b67e679eff8a0759ed7c1e7ce8f9`  
		Last Modified: Wed, 21 Jan 2026 19:02:18 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
