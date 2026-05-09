## `amazoncorretto:8-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:bbbef38f65b9479053cfc82525ab086d0d51c6fb0c7566c30bdb2a6ab5c77983
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d85cc896ad6ffe4b7b1e1752fa3ecbebe1c290397652fe8487be06939aae7386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104560668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9562b295dc701c7ef799b086ae0bc6ca062a06eb1e15a20cd3a5a5edd5605b63`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:58:03 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:58:03 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:58:03 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:58:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b17809d2b091f6dd0558930d7059998acf6ecd42baa973457cd07e8e42bfce`  
		Last Modified: Fri, 08 May 2026 22:58:17 GMT  
		Size: 100.8 MB (100752479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:07fff64a74a042176ebea4afe53352f28f3b98a50913fd4569a261ae5882f92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f08cddab9de5420122f93cb5541ac683b6aa3a67bd9d43c8123719c9659d82`

```dockerfile
```

-	Layers:
	-	`sha256:b162f050e6ba95a0fd08e22bc01db64881da73023f89f816746c4aa9cf8d50e8`  
		Last Modified: Fri, 08 May 2026 22:58:14 GMT  
		Size: 247.7 KB (247674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d75949a9848d12a7db1b6d04ad6c09f05a5ee5f73203c3400f41ababff4af3`  
		Last Modified: Fri, 08 May 2026 22:58:14 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0bfef1435c0aa2bc609378c418d5f152e305205b03134ded2c986023ace0e9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104687265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083c513d670be82fef90e15a5a42147d9201d4a00f5361029f8c6904c9cb5f61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:34 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:34 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:48:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c499d1b2971f31335dc230ae041b6721efbf5a5d133a799a14f8f04c6600f071`  
		Last Modified: Fri, 08 May 2026 22:48:49 GMT  
		Size: 100.5 MB (100545371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2ecdd1501592668416cd61cf2a0c78e978f57b1b73a2e0fd05afb6b42f73abe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778448c89eb5082323d7115597e289a5eead3f63cfa3fddcbacd3baa5c369d8`

```dockerfile
```

-	Layers:
	-	`sha256:4be267dca02d25a56b960a258471fe22cb4d02c67745c3dacdd45992f94e9e5a`  
		Last Modified: Fri, 08 May 2026 22:48:46 GMT  
		Size: 247.8 KB (247806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c35e86175e98990261e4a7fcb8cab499e1f17372ef939e7dfeac81fda5cea15`  
		Last Modified: Fri, 08 May 2026 22:48:46 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
