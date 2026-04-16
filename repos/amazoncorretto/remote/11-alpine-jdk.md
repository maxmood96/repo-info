## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:b0329df497a460a0571978415e3d985aadcc119eaf7eb16e81c0d66097f011c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2de078eaeb4f6dec65cad3b9c820367c2ca2e2c0e76ff2c37c7603ea4dfabcc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147450168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870bcd2064f72361d949492ffa5c9f2451c40b4fdf23bcfd66d64f48e46ded77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:28 GMT
ARG version=11.0.30.7.1
# Wed, 15 Apr 2026 20:24:28 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:28 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fbc81a1c67951c4d530fbb1312c89d9c8fdd1fdab502c0ffd7f5b9683e7a7a`  
		Last Modified: Wed, 15 Apr 2026 20:24:46 GMT  
		Size: 143.6 MB (143585979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75b643696bda0bc0b6d3015a3b9433b7098532b67f1629eff50d3010425f794a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.6 KB (599639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d334fb0336ad67b99c085c62232b63eb72c1ce4a6cf2c409b6bb1d8f3099f8f`

```dockerfile
```

-	Layers:
	-	`sha256:66f0b337ec3131fa03db1bd2712ffdad944dfdfb4028759dead2f85ebac645ff`  
		Last Modified: Wed, 15 Apr 2026 20:24:42 GMT  
		Size: 589.0 KB (588957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba1f82fa9c02fe3a0f989bdaaf05fc3c614ba5858d78e1c431e14c9311ee0da`  
		Last Modified: Wed, 15 Apr 2026 20:24:42 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5fff8a041a04ca91fe63c55d188d8668f2dccd90ab640d09ad83952a8f80007f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146055653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010ef3d23a42b53669a1e615813ca52d06126159a2570927652928271e29cd93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:32 GMT
ARG version=11.0.30.7.1
# Wed, 15 Apr 2026 20:23:32 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:32 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7f15f0553c050361ce115b544e04a69d299081b3ecd16fc7763b671f57d2a9`  
		Last Modified: Wed, 15 Apr 2026 20:23:49 GMT  
		Size: 141.9 MB (141855783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db94977968a6478e1c017d656362db9d9f91d43de10e6927af7068df351f91c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 KB (599245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95106bdbb6ebfa754ec9fecbaa84f783533a51ba991dc59e1d7e0cd96d916dd1`

```dockerfile
```

-	Layers:
	-	`sha256:01adf9839b03f0bbc26d7e6c7b5e1fe9442b3e30fd80e10aaa3c61220906e9d9`  
		Last Modified: Wed, 15 Apr 2026 20:23:46 GMT  
		Size: 588.4 KB (588411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0334d18bd8325faeecabc20e06a9ee906b06214de737f876d6749bfa50c59d`  
		Last Modified: Wed, 15 Apr 2026 20:23:46 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
