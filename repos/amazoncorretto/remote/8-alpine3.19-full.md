## `amazoncorretto:8-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:9549f6b60755b3b1d8a254c0d31e289580ba47a2165c379dbf692fb3bf672eef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2a71a31baebf6b6d314d55a4cd0a4b0c4bf4fb64f4df2d34206d8a259a33d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103610380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2270c28827b2b475a126b07ff22cafc8dc2b2a34022edf7c20452875209a039f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Wed, 08 Jan 2025 03:16:29 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3952ef33cb0738a9cbfd179010cc53538d57caede38249d725cdd2a241f2b8`  
		Last Modified: Tue, 07 Jan 2025 03:16:02 GMT  
		Size: 100.2 MB (100197109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eef69312c96adc5971074f4a42a5b8d6105fa47039dfecd7b9d5f1bf0fa6e420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (255030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54524d79b466aa621a243c738f737d552dbce3701b4a7039b7325a5b1e762d7`

```dockerfile
```

-	Layers:
	-	`sha256:12b0a50c6950479514b96ac5899f064d00cb6d0bc2eb076b9198ce113a9f2c04`  
		Last Modified: Tue, 07 Jan 2025 03:16:00 GMT  
		Size: 245.6 KB (245632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93121e51a352a7bfb51c45bb4acd3ea248763d02682c2af60a7e1854f6936622`  
		Last Modified: Tue, 07 Jan 2025 03:15:59 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d2df845de865e833721c031e10ea88bf5f5c5c7b7e23c2b0b3c500ade53d450c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103331005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aac95ba30a86cbce1e565abd9a8b877017480cb7ac780f929b06bb8e641685`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb25cb3d1da69848e618c80a1605a598325112f494256f5b63fc66fa34e28c5c`  
		Last Modified: Tue, 07 Jan 2025 07:19:49 GMT  
		Size: 100.0 MB (99979057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:57b0cdadf1911f81ee11a23a0f1e33d6a6fa9be37e1397929f7700074733dd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c05e95b641ec7ffc2198dafe18e407f52e59ac6edc2c8ae03f1b1f431289fb`

```dockerfile
```

-	Layers:
	-	`sha256:6dbcfecbea750070e5d189386470adf74c6d78c19c85c6a1ed2af16aff27da5f`  
		Last Modified: Tue, 07 Jan 2025 07:19:47 GMT  
		Size: 245.8 KB (245764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c472cafc843274c9fa8fdbb8bd837e77cc0fefc0a62a51b004842bbf60afa71b`  
		Last Modified: Tue, 07 Jan 2025 07:19:46 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
