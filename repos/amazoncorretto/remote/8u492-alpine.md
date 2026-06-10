## `amazoncorretto:8u492-alpine`

```console
$ docker pull amazoncorretto@sha256:91c3b6cd9b33bfc5928017ac6ffb91be2ce0c1df7d3d344e213257f9626126c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ef3a142294d0a704947faaad5abf0490a9677027cf1718db7a441a52d41eece2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104618075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c11981fb4da5dbc71553fea8e5acf7a4f2f3d4e4275949ff14f63523ac0da`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:38 GMT
ARG version=8.492.09.2
# Wed, 10 Jun 2026 20:15:38 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:38 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa15ff487549bb89981bb7c2873103418ad7229900591056a485b465d2c0669`  
		Last Modified: Wed, 10 Jun 2026 20:15:53 GMT  
		Size: 100.8 MB (100751320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d8d8cd082b45b7477682d5cbd35985414694e4b74c394773442ed4aad65cfa8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 KB (258413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e208cef21d1659a2549e28604cddd2d4dfaebe5a86e726d21b058cf5257f2f22`

```dockerfile
```

-	Layers:
	-	`sha256:86ab85c0de42efd70f9ba969eabfb2cbde9f77b9c089defa5ff4fa0868a4239b`  
		Last Modified: Wed, 10 Jun 2026 20:15:50 GMT  
		Size: 247.8 KB (247760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c29bf26759a71b929df3d55c97d650a90435955c00b911e63b3915568bcccdd`  
		Last Modified: Wed, 10 Jun 2026 20:15:50 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:96fcee7f0fc7d33c76fda9ef51fc7fd5ddd0bb6ffbbd8ad71214f5e9dd13597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104747058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68d0683e4c0c552037c18cdcab29d6da8c657dcb436d1e10c0e20cfdb84485`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:27 GMT
ARG version=8.492.09.2
# Wed, 10 Jun 2026 20:15:27 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:27 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe00d919a24a1ce2e573665ea26c2051bb174f3654fbcc83e2cd447bcda19f2`  
		Last Modified: Wed, 10 Jun 2026 20:15:41 GMT  
		Size: 100.5 MB (100544728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d8c83c523fa4bf328b283e5379884a05883f5cc13601167898188a29b933dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 KB (258095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72a95d9e21079998bb33df9043396a01e9104640e76d1062c7d12742b74f6aa`

```dockerfile
```

-	Layers:
	-	`sha256:de1f3a44b894c008b55c74d10f2d20489467fdaaf01e52ecbfc4cd1d70e10ec7`  
		Last Modified: Wed, 10 Jun 2026 20:15:39 GMT  
		Size: 247.3 KB (247290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8945bd9d07e94ebc518b7692970e797a03f2009dfe711d8cfea7a1a5b3762bd4`  
		Last Modified: Wed, 10 Jun 2026 20:15:39 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.in-toto+json
