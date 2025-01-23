## `amazoncorretto:8-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:e666bd75037c946d2f0418e51956339c7513e9d2347406fe39edb41af8f796d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d7dcf5cd96438f7e4c873768fbd35be60c19f873ff7ac5b28333084300f900c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103614596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa35fc6894417cbd33cdad98f499a903ff1bd56f68067b970aeec7bbdf0fbb84`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f57e41e59d0c9c80fd27629e7c742fb2f4e4d20fab24b9cac2dab0be7e70e`  
		Last Modified: Wed, 08 Jan 2025 18:09:06 GMT  
		Size: 100.2 MB (100196622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a82f2a18e64ad2c642912644c6131b87e2eb7f392cf20b8b649edc57f66e16ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5d8bdd5da1d8997cf4d3555d7b0bf120fc273e8acebaeffa25b34ad9563ff`

```dockerfile
```

-	Layers:
	-	`sha256:47b6ca7dae9b2cdfa0aeccd65c6e8dea2550b7242b8b48b2eea4373b3ebdbcbc`  
		Last Modified: Wed, 08 Jan 2025 18:09:05 GMT  
		Size: 245.0 KB (244973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1dbcf95ade1837a05994c9665053be03731061fee60588ee0440047d986a950`  
		Last Modified: Wed, 08 Jan 2025 18:09:05 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0bb5cf54c49a560c78934e7a4cec0c3d2d322feed64ecf967db9e10ae776ebe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103351426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae894eae30a6515e007ac2984c3db16c19d12e3e8e46b8f68ca7a4e1d75ea4e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474348bcf16d0ae474b5c2ff6a97d4a096364717c5d87a0903a1269455fa7993`  
		Last Modified: Thu, 23 Jan 2025 18:31:55 GMT  
		Size: 100.0 MB (100009565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:58f78a8e88dc62121d4596cc8a44c1fa776b10c98354fcfb64aa1e3b5afb0d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dcd6962c1f8cb006fe0aeddff46569310634d869ade89deea4e8d091ef717c`

```dockerfile
```

-	Layers:
	-	`sha256:c80c2cbb9d1b4f472abe6fb2611c5b9bfd1204906caf278aefffc158f48551d4`  
		Last Modified: Thu, 23 Jan 2025 18:31:52 GMT  
		Size: 245.1 KB (245105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cfd4d2a3ce57e452ca99f24df233249da398ad979ca2f57cb4bf5f646fdad85`  
		Last Modified: Thu, 23 Jan 2025 18:31:52 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
