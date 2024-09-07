## `amazoncorretto:8u422-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:eaa0802aa6d7f374897c25ecc786315f16f0290f38e1511a8a010ba12e870b0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d66a2dba0e72189c58d280f28f99e66968d9f328000f3ab447d2144d3be199a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103515959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6cb41e0eb07c8ccc6fc69d8014111b6ab90c3dbbd8b81afde3e6312998e45`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac45a1b3328851d3a69f841b16c469a5c65d8453f58c091d793e936e6aefb5fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:38 GMT  
		Size: 100.1 MB (100123765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9dc2f3640f36c209f375f22c019fcbc59fe8ebd752fb74e384d78b871a9cf815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b129dac7c45c0d2202f739026c94121d9d8fc40c78f62fe98391d4122d6336`

```dockerfile
```

-	Layers:
	-	`sha256:857ebf6e1e7e05b0bbd551d7e1447c253f4c02139db719d636a5785439b78d01`  
		Last Modified: Fri, 06 Sep 2024 23:25:37 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0671cf9bc2ff4009fb04a8c24b86df6704e9039b294e0ff3b26b6b67530008d9`  
		Last Modified: Fri, 06 Sep 2024 23:25:37 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2ccbf7dce7779b7d1aee060fefc33b87de121746ab641aef30fe6a06c9aa5203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103111811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6776093cdf7cb8a8ffef20bf926dec57292c0b2a894a26bb132b3c9970f96ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81b4fcdafe61d9b3396f82587ff77ffa36e6149c73af8f4c365b2d718eb43ff`  
		Last Modified: Sat, 07 Sep 2024 12:05:05 GMT  
		Size: 99.8 MB (99836739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:caebcbb3c937fff85bea40757fe7a43c07ec8fd3d8fd0e741f5d4e210c84cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 KB (254057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9e24eaf9d5ca364a7e583ba96b87ca64420489826207c6a179becb07903cdd`

```dockerfile
```

-	Layers:
	-	`sha256:75712400d3800cb1238d6868313a5f07ad7844974d26a4611da4264d89f3b0dd`  
		Last Modified: Sat, 07 Sep 2024 12:05:03 GMT  
		Size: 244.6 KB (244605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57457389d6bf1b6fc86631b115900efd8fbc67cd20ff2a7ef191ba53b69dd12`  
		Last Modified: Sat, 07 Sep 2024 12:05:03 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
