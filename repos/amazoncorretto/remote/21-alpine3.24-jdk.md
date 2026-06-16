## `amazoncorretto:21-alpine3.24-jdk`

```console
$ docker pull amazoncorretto@sha256:30b1b2246cee9a98c9bf8a11537a04f1eaf8c59279b0c70ae02d7e5b934edeaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:587f762f9434bbc18397adbc5bdcd8712672d53993a6fec1d7af219ed1f80fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165683610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc94082041cf096e55c094054ad048ed42f2b35506a92e650d493c68fc28d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:27 GMT
ARG version=21.0.11.10.1
# Tue, 16 Jun 2026 00:19:27 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:27 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989fc81d937729a00dafca55dbd23dc5a68a72a2a59d2f999819aa71fc5c941f`  
		Last Modified: Tue, 16 Jun 2026 00:19:47 GMT  
		Size: 161.8 MB (161837219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:832e2292f3c878a82d7514223e827313a6e637fcb9b56639f79efb4af22448c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.5 KB (594472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4076146db122bb900a9344839dd08850e1aa0888d2b42283bdcfe312bf30fd24`

```dockerfile
```

-	Layers:
	-	`sha256:67438969fc5ce08ec367d1581a4a3860247890fbd5513a00679fac23f0cb31f4`  
		Last Modified: Tue, 16 Jun 2026 00:19:42 GMT  
		Size: 583.8 KB (583785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570e34f2eb8ff2de89d80d5051f174624ef05b7d91ba7cae458250c50aa3ccce`  
		Last Modified: Tue, 16 Jun 2026 00:19:42 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dc43b39c47f1729dc772a9b8af7222757fac6c8cfa8a0802829af665b1c89925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164024782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9a2608a3b6e369b406dff44c78d437e4278669be74c8f79e060696f26d6a09`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:35 GMT
ARG version=21.0.11.10.1
# Tue, 16 Jun 2026 00:17:35 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77b0e734531ffce2dd53a41d8efbea96cb25eff325d8480cac6ef130b7bb81`  
		Last Modified: Tue, 16 Jun 2026 00:17:54 GMT  
		Size: 159.8 MB (159841745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14742d4487c819e19bed3785c6aab130a62752b609a35b6ff8fd399b7c6b2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 KB (593441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ce0c9f7e9febab9914518625249a1f82033b6266ec395b5254acfae94f38a0`

```dockerfile
```

-	Layers:
	-	`sha256:e4afdee34de2a01bbd4fcbad4d554d5533a26fdd94d971094ad1f956c7e5d98f`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 582.6 KB (582602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cd5110d80de58a9c705b135d24452be6bbbfd466f7f0b92492dc9d7957b2e8`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
