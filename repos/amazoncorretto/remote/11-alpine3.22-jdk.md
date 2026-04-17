## `amazoncorretto:11-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:92824cd9d6bf5842d24de2ac40a0c72a9e40cb48c829cafdc9d9c755bf9ed44d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:969c63a80095267452ba5d467edf82c25161bf978c3dcaa2696d826320c3fe6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147397887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1b35df96843577985031e609cf29949ad4b42bd6e43b10ffe518ebcab37c1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:30 GMT
ARG version=11.0.30.7.1
# Fri, 17 Apr 2026 00:22:30 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a78855fbc8045beac37930eeac24b583c2bc7d404567d34f08c3bbd21fa79a`  
		Last Modified: Fri, 17 Apr 2026 00:22:47 GMT  
		Size: 143.6 MB (143589698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e1b3844fa6eabf236d40a8626758c90880717cf5e6bc6feb7f966b0c74b2430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56dfcc0cf71fadb87b39178219da79a7a1df4dec32fc375d80adc03308e64f59`

```dockerfile
```

-	Layers:
	-	`sha256:c6bfd3338d8e05a7dccc87ee137cd9fd8182109d6c8fcd5ae7ceb9d74b34c606`  
		Last Modified: Fri, 17 Apr 2026 00:22:44 GMT  
		Size: 588.9 KB (588928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996b827b83cbad72a9d23edeb00b60dd74b7eb9f7e75ec27e2ec2a34f5d59f5f`  
		Last Modified: Fri, 17 Apr 2026 00:22:44 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8e67598541de5b1b98f17b9877361d895219cc8bc5a35618cf7c6188a164898b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145996281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e33fbe8743b976ab72571f8c1c058d4cdbce6502cc97331eb776db89661433d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:39 GMT
ARG version=11.0.30.7.1
# Fri, 17 Apr 2026 00:24:39 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:39 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cffc6fb24b7c511ac9c5ed13a8d811f33e5ce28afb90def8aa490bc7f45272`  
		Last Modified: Fri, 17 Apr 2026 00:24:56 GMT  
		Size: 141.9 MB (141854387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a85a1b4c9f8a3688b11691ce2f254f89d96152dd345cbbf8fce4d55d149ccdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1b48c63d9745933a96d900999d194747050e8aaa90c05110bd03060c15d6f2`

```dockerfile
```

-	Layers:
	-	`sha256:6a6fcad14d2bb5815a8f9479f5c27d35ec90a6866bf3fa9cd64dd746770683c2`  
		Last Modified: Fri, 17 Apr 2026 00:24:53 GMT  
		Size: 589.0 KB (588984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660156c8cbfe5edea7045f634cf6e58bbd86b8043683d12bf97366cf5236506f`  
		Last Modified: Fri, 17 Apr 2026 00:24:53 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
