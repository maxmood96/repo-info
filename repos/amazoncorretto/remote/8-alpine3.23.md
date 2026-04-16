## `amazoncorretto:8-alpine3.23`

```console
$ docker pull amazoncorretto@sha256:27d04fd6b11920aceca6c32f8a8619cfc9635e4abe2076a36bc62ddf3ce211df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.23` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c5055f0d47e4852544c9e4a41d4c41a1e3f45a7be38eb25eff10cf2ae7e2ea0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104641083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c7dfec29259c53fda8ca4d1751953ae39d72a16b9ff0071c0b5031de6e7d44`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:14 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:24:14 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:14 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88d1dcb40680cc470fb6c04d2b258ef4349b55286064027930674dd42c7a614`  
		Last Modified: Wed, 15 Apr 2026 20:24:28 GMT  
		Size: 100.8 MB (100776894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b82a5109b7a07c92ec3dc1640d0be75d8082901f561109e3762ca7cc0261bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 KB (258346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb0c43bf6a4b4b0fc002639d08d0e516a80c1347d752a54e074887edf28ba1e`

```dockerfile
```

-	Layers:
	-	`sha256:3e3f0ec9d8f2c248dec99aeba53f74830351baf931a981addf785b5e63a16649`  
		Last Modified: Wed, 15 Apr 2026 20:24:25 GMT  
		Size: 247.7 KB (247693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a98d86e77c7fb373af7ee6332f6eb0990986b1229da85b97db24a0e7a76290f`  
		Last Modified: Wed, 15 Apr 2026 20:24:25 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:60c577d1666e69c3f1488e8b7f99a6d0ec9b976bd6364b8ba0c1394586947a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104763470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb282b004576011f127bd95ce765c360e430b14c338c316f9d80afa8c85d34c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:20 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:23:20 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:20 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d31962388d49f10d3593e394a384b818c01046e78cf4213c87494773368e25`  
		Last Modified: Wed, 15 Apr 2026 20:23:34 GMT  
		Size: 100.6 MB (100563600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ec862633e031c94a7930c3c6164ddf9f09772952577d232dbcd96606ec37bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 KB (258028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da5bd5ea7ba7ae29ef52de2c28dfce944e9e281f4ec89863cbffd2695cb31bf`

```dockerfile
```

-	Layers:
	-	`sha256:520a7fbef69d6b56e418ee0b1926308d3d43eff902ee439af65de4ee64748a40`  
		Last Modified: Wed, 15 Apr 2026 20:23:32 GMT  
		Size: 247.2 KB (247223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34265b5e18a1ad4a40c5c24cbfddc06fe85e3b59f9ddce095887cf6576ce6742`  
		Last Modified: Wed, 15 Apr 2026 20:23:32 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.in-toto+json
