## `amazoncorretto:8-alpine3.16-jre`

```console
$ docker pull amazoncorretto@sha256:96cfef66c03dbc96898e2fe6530171b7d011540be1d451b1f0106644364f919b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.16-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:308823146eaacec0b102807f1ead710f356cb1c7396415f2849f61e100f8a071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44455249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816f7ece94285b097b902e88fe96f0502b4c1e338e9d471af17e433b767540cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31272219a70b23d91008d52c282d8bb3d30cf0cc3c0888201835a139207f283`  
		Last Modified: Fri, 05 Jul 2024 19:55:58 GMT  
		Size: 41.6 MB (41647412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.16-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ca94192c6b1e8e35d2f63e59dd253a910901cdc6eb3527acaf05e9c229691b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 KB (184544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556586ce20a7aa1a0144bc48d6b145ca1a6cf028a8bc9a133fc78a284c5b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:ed4b788c4df195aae7c326e7cc2a8ee13980d1636c8f1fbc48053608c4a14834`  
		Last Modified: Fri, 05 Jul 2024 19:55:57 GMT  
		Size: 176.1 KB (176090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88894d2337e0afa5100ead290ec67d02e869799152b6b9f7c8f40baa182b3d0e`  
		Last Modified: Fri, 05 Jul 2024 19:55:57 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.16-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5c01a1cb59328d5b7130f3439efd1e0184a4a6428e2648213516730daebf65c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44007994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f71b2b90d78854e85b22cbf1aac3e86afa646977ee1c996344db4393489500`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74437e52c601cca21b6fe525e031820ed148e00a446c74fd536a3c59d31e3bdc`  
		Last Modified: Fri, 05 Jul 2024 19:59:44 GMT  
		Size: 41.3 MB (41299711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.16-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c8d3b024fa5dad44f64cb0e4c7bd9f74e3c87f3b9e3bf70bdc680ff856032ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 KB (184928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ea65231bdb82ae2383011ab72c43c16bdd5fd3598d6b1c865b767e3655138d`

```dockerfile
```

-	Layers:
	-	`sha256:9766f22b178fd10d5e8d99eeb4fa489a9acf9925a788f19bb2ed6e2d3ca14d61`  
		Last Modified: Fri, 05 Jul 2024 19:59:43 GMT  
		Size: 176.2 KB (176198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cba82167b13d92439e673bca9b93482eee38d253950005b16c3b0069e46c7a`  
		Last Modified: Fri, 05 Jul 2024 19:59:43 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
