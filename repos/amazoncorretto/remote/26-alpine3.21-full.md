## `amazoncorretto:26-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:6df3e4c9699e93729093f7dab713f5d844660256fa6836bc054c46d34bbb09da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:31b089885b6c2ba1b7edffed6f541a30400e13b043be1a114000a714b9d8a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188573988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af98caae861bb22bd5e52616cbb407603a1a964abf935b920bf13766174f483`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:52 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:52 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02328661b23eda055423cb70cde1453feb84a4e3536b760035616fcd0364b770`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 184.9 MB (184927113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c9e40dda4e5ce07c0cc3bb32d254609541a06f6a5363d198beccb0bd2c70254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.2 KB (600222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aec7ae003fa4f6d4d69a8388bb9182c79a7b56f9c7c09f5da6c937555e3fdf`

```dockerfile
```

-	Layers:
	-	`sha256:c117c50286df09d33397e928b354ed9e39d039f08e1b27171ca69bed1702cd70`  
		Last Modified: Wed, 22 Apr 2026 21:36:09 GMT  
		Size: 590.9 KB (590851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf8940af31863daa9aabef6b4783acf35bef092e8c8d361e45cde6ee9f821b5`  
		Last Modified: Wed, 22 Apr 2026 21:36:09 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6c0589bcd13941a8276203de14212eff104e4fd02b0adbf675879a2836f314a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186491687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ff502ea719e0b5eb26c2c0c170e23b1a9f5724d43aa0b79b0f5a0a1655627`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:56 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:56 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb756459627d51cc4430d8fb3d0d36a1e957a29d0fe530447cc9302ec1dc607`  
		Last Modified: Wed, 22 Apr 2026 21:36:17 GMT  
		Size: 182.5 MB (182497222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9b7f02bc40b2eceff03c7049869af33294974cf2d377279342d0b5c92fe8b1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62df100b371b46f5147d6815770e1a7bbbf5ca4bf01d5fbf269cc17fac534244`

```dockerfile
```

-	Layers:
	-	`sha256:8673c9ac2f252f8657cb252fc2f5d0968c0a26ef6f72a13591a2182229f5ba0c`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 590.3 KB (590267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4f9288fa7c313d5e92e11b64e15db698ee45373b9f4758c4543360153ec7d5`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
