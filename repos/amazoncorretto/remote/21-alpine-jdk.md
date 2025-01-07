## `amazoncorretto:21-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:e9f0d377f2568ee5990552800ac5de0d1d3e872f1bf5bf4728097f8b7b805b34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9fdfd832bd43e0b64c9ae4f4bf871fec78fc6c04726503e9e093ab0d7a6c1cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162544108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7efa4b39a0a0851b35722b38e1e7326d2dcd8999af30952dcebf30377ee0844`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5eaf144fd07fa577b4bbd9fd1e553976ccf28625182105d96db8000bd93129`  
		Last Modified: Tue, 07 Jan 2025 04:20:14 GMT  
		Size: 158.9 MB (158930109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6b217245ee349675ca86c8203706aa4a2c1b0907d6ed7870d8fa7c85f75d3218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bec34ce036365b719f16b6417cb9b5c9ceb8af1b918b13b9fa22fd999a98ce`

```dockerfile
```

-	Layers:
	-	`sha256:75eb83ec0f610e95712182b3e0feb3f33fe10158bc87c11a8064170fb3d2c6a7`  
		Last Modified: Tue, 07 Jan 2025 04:20:12 GMT  
		Size: 377.9 KB (377868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f80665c783961653698f491e2d024f478d8dddc142f8d6b3f3b76eb04ca8ee`  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a1baff800c62ca66638aa50c2a42aeddc1a8ed856265716052990950eb64e286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160967815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00943b443b37e79b13b6e8fd4111f5d5e2b7859721764b201ab1b1a7e405e0f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204f41bc5b0b52b89a1e69dff490ba86e013e780b9832889254fe40822df6abd`  
		Last Modified: Tue, 12 Nov 2024 11:12:49 GMT  
		Size: 156.9 MB (156880089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2b25adbd8670a8286171921e34fe87ec1f80e0cd37ed4b5774fcb362159e8cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 KB (388831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f5b3caff542a755f939642a8058418c30fda93e2cedf4960e3cb60acc8adbf`

```dockerfile
```

-	Layers:
	-	`sha256:c81dd4c126c80d3c20a92a5b509fb4a0507a0c273215b7ce1c19efb8b8eb9000`  
		Last Modified: Tue, 12 Nov 2024 11:12:45 GMT  
		Size: 378.0 KB (377958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82ce3967d37c4c505314f8e993c41ed84111487e40b0bdd81c5b50ad1089dc3`  
		Last Modified: Tue, 12 Nov 2024 11:12:45 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
