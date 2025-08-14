## `amazoncorretto:8u462-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:1ff96c186d353f6fb483b074e03c20b86157dc0fadd4b68ec6707fe08cc9a5af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c78ccbae87e06c96578b7fa58c11cbf6844c933e7ad5107339d8f3e653edbbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a3f93ac48b708ef653a76003845295da4ccd8fbd634372fb3fe60875c1ef0c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f841a53b1ce989cedd63c953bad005a69275ee2b8be25309aba57ea3c69ed557`  
		Last Modified: Wed, 16 Jul 2025 20:24:53 GMT  
		Size: 41.7 MB (41730571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:771fee68c9a3dde68390f599bc4aa9d0defd12530f19aafc91efb033668f436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a1fe03dc336d81986dc15aa88fcc316d7f99445771bebe664e17d8fbce2a33`

```dockerfile
```

-	Layers:
	-	`sha256:c46d0d73c6d57b002bc73d9466ae98948b34bd4fe665f65bbaf1b8873746938d`  
		Last Modified: Wed, 16 Jul 2025 21:51:46 GMT  
		Size: 182.7 KB (182694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653cd9ddb39d318ab7626e600e328eb58c547de1a76c9ed064985ce0be84e018`  
		Last Modified: Wed, 16 Jul 2025 21:51:46 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a649ce7ff7ce1775cd1477e636c55d3af80a2fbcfc36cdb830f42684a7729a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45525055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419f2ad46587fd8bf7d27cbaf3afed8e61b5031141ccf21d70a2f215cc3d3005`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c233b5a9bf74ed0feb9d26a2ad2da9121522a2b14007ccc31569ec674c0e6c8`  
		Last Modified: Thu, 17 Jul 2025 01:47:48 GMT  
		Size: 41.4 MB (41436687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b529039d242e7f210df4c8bc496083b7845c753f0be0512416d2e2902708b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 KB (191581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9003660a4e92049dcc4b58609cdf60f0c8e44a0ca680f38a3c5634e7f1ba97`

```dockerfile
```

-	Layers:
	-	`sha256:4eb4a203f2b632541a90e3f6455e0e22d3e308ff09879d5ad72e7b143ee1daaf`  
		Last Modified: Thu, 17 Jul 2025 03:51:38 GMT  
		Size: 182.8 KB (182802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a91965f7c55f57f7011053bb57022028380296023c1c0757c8a43b1d6fec586`  
		Last Modified: Thu, 17 Jul 2025 03:51:39 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
