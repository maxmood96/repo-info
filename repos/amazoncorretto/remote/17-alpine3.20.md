## `amazoncorretto:17-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:1b1d0653d890ff313a1f7afadd1fd81f5ea742c9c48670d483b1bbccef98bb8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3533d791fb8d65421eb2c618801166a1214829295bd9f321deb6b9d1fea2a558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149640983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a65120632846ef206aa1d7943e5264f37866546bb69de9d2bd2efaff6b9b34`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df6b8604693f7a571bcc1570a83ced515ec48d5c7fa62427f8be767c8ef35b`  
		Last Modified: Fri, 06 Sep 2024 23:17:39 GMT  
		Size: 146.0 MB (146017176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6765567f290f27afc434e07b5becccaa2212039a27c6bef168abf70d8bb20956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de16a567d95387b4f242eb3569667c62ad1eb33a4952a1da1d4163bba47c90c`

```dockerfile
```

-	Layers:
	-	`sha256:bc44f4ce79c3536544a85b524a1352df58deb99c50e6e37ff9ddefbeb9850f68`  
		Last Modified: Fri, 06 Sep 2024 23:17:38 GMT  
		Size: 377.8 KB (377836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302d10aa1d821a8f77c124165d61259c62b4d97335e85a57a2e858e240dfdff0`  
		Last Modified: Fri, 06 Sep 2024 23:17:38 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1be973a14407ae5b39b3eed54f5c6722764f0cc99611cc9b038059259bdd94f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148437126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438ef6e2e3491b41b3e0e8ad4d253e5dfae4e806f40416dee7f60bde93ce29c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d9aaf86ffad08a7e7ddd7de2167b4cfb8b32194e5356c6d96e709169dba604`  
		Last Modified: Sat, 07 Sep 2024 12:12:56 GMT  
		Size: 144.3 MB (144349480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ed917ee3d20f0b85f655fa731d1c0620a9b797976f897970ad51c9a3778339b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 KB (388129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2267d84e831bbd88757b41491c57b9fd5845a8ed61f6a563508c68c2131ebff0`

```dockerfile
```

-	Layers:
	-	`sha256:6a39a6571eeca015e05f99149c95ef6d2770e3fba2e37b2cb3349a2c5db28911`  
		Last Modified: Sat, 07 Sep 2024 12:12:53 GMT  
		Size: 377.3 KB (377302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023d661e1e9fbc3cf0190519ae0b72972b59b76bff86147c7637c3faa8b80705`  
		Last Modified: Sat, 07 Sep 2024 12:12:52 GMT  
		Size: 10.8 KB (10827 bytes)  
		MIME: application/vnd.in-toto+json
