## `amazoncorretto:26-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:1476e2353d81c23f84e0b9c87a9489c841c352c6cfd3dd3aee8505c48f6eeeca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:28d289273d5c1ed5fb81355dfb39672200b4f9d3563de57c659c123cfc507f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186626928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8226a50d3602e986f7dceb7cc79a2d603bf2e5bec493fa071850049cb533d59b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 22:59:44 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 22:59:44 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 22:59:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 22:59:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13388db833b9fe6bf98fc61f85c82aefee1cf0e76da4fa1158e20b69e2fd3382`  
		Last Modified: Tue, 17 Mar 2026 23:00:06 GMT  
		Size: 182.5 MB (182487409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2f6c2f4789e0ac3ef223870d4bf965227ddd6c8181cb172bcfd7eda96c6bdf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543140b7921cd56395d4313cf582071b7f4718c58aa76e0ae79e32394dc97add`

```dockerfile
```

-	Layers:
	-	`sha256:1816081c0a28e2e6ce71baa9c06d619bd4fab2a204775acb34a4a2434cd7ef1a`  
		Last Modified: Tue, 17 Mar 2026 23:00:01 GMT  
		Size: 587.0 KB (587002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b4c7394b3bf0d96280cf3edfdd89ce24fa8a9ece02b4a4e7c3ef72c2eab0de`  
		Last Modified: Tue, 17 Mar 2026 23:00:02 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
