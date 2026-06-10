## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:b8b0033a9be4a5565bc84fadabb5e3ebab4e37f168c994c421194a1d3d8c0c15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7f7e03138688f9d3ea39cfbf1447be09a2d4412a5289cbbfa4b4dc31f3a6c30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147578718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af665f703c7c37d040dcd70ebc8c617a7f7a4ee09f625473f32b7ea9b5fd1813`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:49 GMT
ARG version=11.0.31.11.1
# Wed, 10 Jun 2026 20:15:49 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:49 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d04effda964526869660fe966d635bbee77285f6f89e1106279420025648842`  
		Last Modified: Wed, 10 Jun 2026 20:16:08 GMT  
		Size: 143.7 MB (143711963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:37043e7d9fd0e4e46f7b7b4ea24ceb68865e62674949fdf67e21c3e0c12747eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8603fe17bd1cb21d2f53c9140f2e819f4ef260e558ddd9b1eb0b39c37ceaf3c`

```dockerfile
```

-	Layers:
	-	`sha256:031adf3527d6a956d57117739a8df86a0760077099d4203d86d05ea26a35879b`  
		Last Modified: Wed, 10 Jun 2026 20:16:03 GMT  
		Size: 589.0 KB (589030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53e899bbed996fcf891d7c3b7f3c97325772288585cfb3df8d456b8ecc420d92`  
		Last Modified: Wed, 10 Jun 2026 20:16:02 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5253421cf458bf2a2620e03b77cecbce676338573d738411a4f181fc49875cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146180183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdb1a851c675938b15f027bb072947846d97cf9daf2edf0640a8b0b21e599cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:33 GMT
ARG version=11.0.31.11.1
# Wed, 10 Jun 2026 20:15:33 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:33 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5bb301ff4f081ce472e885a56c4067cd7da3c19072d5daf62f6b12322c7bef`  
		Last Modified: Wed, 10 Jun 2026 20:15:50 GMT  
		Size: 142.0 MB (141977853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2cdc8df2033ee6eb4a83bbbb9945e53af322ed4f6e1533be6aa5be85ee4e539a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 KB (599323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72254e5ed73da0e298c9807b06a905cbfd9fc2553d2af2a3a771c8c13e7b7f1`

```dockerfile
```

-	Layers:
	-	`sha256:6dd67ba71a7400bc1c280699d19ae76c26ecbeb239b671d5a7dc31e5cd051098`  
		Last Modified: Wed, 10 Jun 2026 20:15:47 GMT  
		Size: 588.5 KB (588484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922246811a8810e121aaf9f19dcca45b7d45b835940df55e3d87841e0709a514`  
		Last Modified: Wed, 10 Jun 2026 20:15:47 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
