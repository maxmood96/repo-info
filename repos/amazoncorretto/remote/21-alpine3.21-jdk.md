## `amazoncorretto:21-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:e3488be9eb2b8590ce602d8a1956120322f3b1b76147e64ed56293df449abf14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c82701d37271d4e256f4c2ec34ef205e17f78006023477d662b17e66668aaef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165230856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f917c14f073c12cf36b3b883301b8baf2980523f6c59c86d38f903f8473a397d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:22 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:49:22 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:49:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:49:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:49:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04bf1efc378da2cc76cc6f805928dbf3b8b5916c6ce49f0ecbb3143e96c3c4`  
		Last Modified: Wed, 28 Jan 2026 02:49:41 GMT  
		Size: 161.6 MB (161587114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:35850bb54220c0ff1bbde38a79307cb5a5c19415185a6313e3dcd5612ae9cec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 KB (595836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba80cde1f3a428065b9987ff0cfa38bc1795570317ef92ecc6c5238dbd6045f`

```dockerfile
```

-	Layers:
	-	`sha256:a99fb2b126cf1f08650628849c7ff2ee58c6cad1848f160fa408eeb2bc9d1e4d`  
		Last Modified: Wed, 28 Jan 2026 02:49:38 GMT  
		Size: 586.5 KB (586462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d61dbe84e0323493cdd08d4269c69539395cbdd50d43401f6509f341514c37`  
		Last Modified: Wed, 28 Jan 2026 02:49:38 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5bd30a10bf5843a1063e89228ac7ca61bcf05f75d330958da619f99fbaf9379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163599932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f613d9d00a1e1b362ba33c2f176628192c2fd32f2ef697434217abb0f518146d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:29 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:29 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:29 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899c345535776ba12acbb676363315fada31508e7338c5ed54bd739b29a3d2c5`  
		Last Modified: Wed, 21 Jan 2026 19:01:49 GMT  
		Size: 159.6 MB (159607579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a8324f9329b5f0ca52a225a391b91084ec90138ecf9a981e424ebfbd4dc1ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 KB (595359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fc03e3672125a1d758534bf3d8f04e21babf1421101b4be87b2942b4db7fa7`

```dockerfile
```

-	Layers:
	-	`sha256:9d923fe0f26c1ad9f88bbabb9e650580609469be57f93440d6492274647f2738`  
		Last Modified: Wed, 21 Jan 2026 19:01:45 GMT  
		Size: 585.9 KB (585881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759c3b973702f66a672aaa218748a617f7816bc0890f54873fe29116270ac279`  
		Last Modified: Wed, 21 Jan 2026 19:01:45 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
