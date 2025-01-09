## `amazoncorretto:8-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:6581d36fe801e7c76883f72b0a7d81fbabcad39f04a847f56278a51af8ab2fde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e17d115061d7d5f5206a3338d356ab6b8475922af9fa951ff70c1c7347fd6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103617481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4100d92022c968ba3d20d04978b06f3ecbaa592049ae6a60151b7e0ef5908a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dcc628e7045df83865102b5a21f89001c7724fd2a4e8ac68451492e90c86e`  
		Last Modified: Wed, 08 Jan 2025 18:09:26 GMT  
		Size: 100.2 MB (100197239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44ede2b48a6faaf7d330db646a2ee8619319630abba8ad70179732d5a458a149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (255030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f479d95354b42ad49249a28e227f0a4f94d90ef58283269d833fd5a72875860`

```dockerfile
```

-	Layers:
	-	`sha256:fc434b0b2320f2ac96a6426b0808b9842fe5871736f3c41251b473889b21a090`  
		Last Modified: Wed, 08 Jan 2025 18:09:25 GMT  
		Size: 245.6 KB (245632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d5d87ec5da97ab7572c50e316ee98df96020f4cccf19885336ccd35913c54c`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19` - linux; arm64 variant v8

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

### `amazoncorretto:8-alpine3.19` - unknown; unknown

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
