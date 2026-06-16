## `amazoncorretto:26-alpine3.24-full`

```console
$ docker pull amazoncorretto@sha256:c232ebdeb14ffcefb98645016cee3247bc11bd8770505b2dc23ec691a3712f7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.24-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a7ae7095d9c12ede1de498bfbba26bbecef8675e8e8246916ab4fbcf60f79879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188803085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68af8e0426a4a5649e8e58969f93e3310b57eb37d809c2b22d299becc8a78d9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:37 GMT
ARG version=26.0.1.8.1
# Tue, 16 Jun 2026 00:19:37 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c8c3b9a828ffbfe93272ed9ce3c88af09dec5cd2638cf51e4859969b34845`  
		Last Modified: Tue, 16 Jun 2026 00:19:59 GMT  
		Size: 185.0 MB (184956694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.24-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:12c4f2260a6c4a3565d573e45d4dc724f60cec9e4db29e239748e26a1ac8eb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.4 KB (598366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802c4ec155dd392f5c9ebf0898af57a067b627f11c22762e271d929340c949f2`

```dockerfile
```

-	Layers:
	-	`sha256:f4f217b372f6c98c873b4537411e8c2a5fb9aa01e3ca89213e1bb00c0fc2be76`  
		Last Modified: Tue, 16 Jun 2026 00:19:54 GMT  
		Size: 587.7 KB (587690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c533d7f9c6e53564a3e30f2a1835ba4496ce22a3ecd317005b34d337c73bdca`  
		Last Modified: Tue, 16 Jun 2026 00:19:54 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.24-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5b22054b6a7d321d14c626b6c8840b9906390dc43725a4eed0bbce30cd4863e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186702954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33baf51618b277476dbd1f73c36a22419c932f23b87d1b4dbba6028bcafdac4b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
ARG version=26.0.1.8.1
# Tue, 16 Jun 2026 00:17:59 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03ef00629a506c8dc2f4ffec8b801b436c02986bf2c2a8887397410fd94cc5f`  
		Last Modified: Tue, 16 Jun 2026 00:18:22 GMT  
		Size: 182.5 MB (182519917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.24-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cc845bca04145f8eeb49ff3bcd982c89c2f0cc9d9e2da7a7e8960f6dda77305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 KB (597333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a5621d650cec3aef7bfea0e8afd7548d2b4bd9f02b5f49f2574224c2a807c7`

```dockerfile
```

-	Layers:
	-	`sha256:7fed87679875f1571ad339b0f485a3e224b3c0d635e68e0d5fd954ce603e92a0`  
		Last Modified: Tue, 16 Jun 2026 00:18:17 GMT  
		Size: 586.5 KB (586504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f5b51ab00ee820aada07009125ec17b293bc1f562a1c105b0c0e8eb5daffb0`  
		Last Modified: Tue, 16 Jun 2026 00:18:17 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.in-toto+json
