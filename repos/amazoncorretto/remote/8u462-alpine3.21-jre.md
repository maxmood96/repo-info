## `amazoncorretto:8u462-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:6194ed94c952c9ae55dacee2815cc56fe0dd2c69ab2473e0f0381d73aeaed272
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e01fd55b4ec2232b643d3338e017473a6dc63ab6bba0fae17a6ac6b98780a7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45374205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079eb07e7aa8d9399238eeb80a89ad1f5323cc96c7bce417dd70dfae3ce6589b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797f30503ab3dba316c71cc2ab282bd4ac07db992398cdbbe48a37c0dee9df12`  
		Last Modified: Wed, 08 Oct 2025 22:59:08 GMT  
		Size: 41.7 MB (41731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:08950be0a27d2be8fbafeabbb4f814f4eac4f7d4adc3f47dcfc90b227a01d3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208b880ac351d94132b1677a72d74a13da98dc47ae6a4d90bc0e02b54a9da8c7`

```dockerfile
```

-	Layers:
	-	`sha256:85ccdd0f7b112cc3377c021e520a37fe2ed44d1caf36d4508391c88aff9e889f`  
		Last Modified: Thu, 09 Oct 2025 00:53:55 GMT  
		Size: 188.6 KB (188597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cf5fcabb5924840f2ace84a44993bd1b3efa3b6eb9f702c809bf8a443f5105`  
		Last Modified: Thu, 09 Oct 2025 00:53:55 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7d5e71a8cb9466df0420118ebddd040112b1d1e83fbcbcc3e4aabb1a49a2baf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45429420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea2325638f9a97704a6836ee352a85ebdfcce5f1bdbdb97756eb66b4ea5d9e5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10713bb5cc032d2224186949693b3ea6ed71e2eca9548568af1bf230ae47cb2`  
		Last Modified: Wed, 08 Oct 2025 21:46:29 GMT  
		Size: 41.4 MB (41437067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a7588503adf5d24b54856a47c8c919cfc14f8b22231853fbb7d33d8683bf076d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 KB (197483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac51120a23dfb80d9dfe90b56f0601fc56f4ef213dd0f2c297269fbb39dd28e`

```dockerfile
```

-	Layers:
	-	`sha256:1c6dea89b564a0c08a984dc58e521486d4c5b544cad31eb0d0467153407d79b2`  
		Last Modified: Thu, 09 Oct 2025 00:53:59 GMT  
		Size: 188.7 KB (188705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02382950450834e67fbf5606f4cabc82799b292376182e21bfbab2dcc12bde7`  
		Last Modified: Thu, 09 Oct 2025 00:53:59 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json
