## `amazoncorretto:23-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:784e12f4af491e78294bf7e85d0b8ff50e1013a97bfd051a176ebdeb278c986d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:64ff0ca1ffa352fc15fc97de8a644629b041553deef4cbd826acca8d8a42957d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170074933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eac1f26583bf96d85e07069c703a6404a2366304a7912583fe181a84d9aeabf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195387818aaf6c946d164151b31daeba708b5d1103fac930ca8aca3106387e15`  
		Last Modified: Tue, 12 Nov 2024 02:13:17 GMT  
		Size: 166.7 MB (166658532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c38adf7f7bb322b90605d4a9c768c2ccee742a747e5088ee2dd637aebe3a403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37888d639bbf3127cb6dca9b70d5e0465bd6794051f61eb4654559c3b17dafc9`

```dockerfile
```

-	Layers:
	-	`sha256:79960cca74ceb1cfb016fedf402ba2e7206f7795e88b411f6444a06757d5b352`  
		Last Modified: Tue, 12 Nov 2024 02:13:12 GMT  
		Size: 382.7 KB (382709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb3511adfbe23ec9f97ac384eabf12016f813611f96ec649f701884786494b3`  
		Last Modified: Tue, 12 Nov 2024 02:13:11 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:974ed3552715194fc35a0eed2c27848e5602c81ef7b0774a16caf4d5c8e34dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167693581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14cd9084dd086faa1d2e1cc9c18ec6d858ff8103aaeffc600c9b1acb2ddc240`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555b3edbc635eb7e13c6a301daf596cbcfc4702681e4b56ffbd52b26c73bba12`  
		Last Modified: Wed, 16 Oct 2024 18:44:39 GMT  
		Size: 164.4 MB (164353234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:503b5e2ba6007ea72abdd4a7e3a62be28cd8b5b5b0d0ed533a5a68f761bf26c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 KB (390698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9bdd2fcc5d4c1bb1f67bd8786c98113778c6ab56c54ffa0f6217e2c67aae38`

```dockerfile
```

-	Layers:
	-	`sha256:5ba68b57243c1248f55052d454c97847eec85482691964f1dc72556f54e22a8a`  
		Last Modified: Wed, 16 Oct 2024 18:44:36 GMT  
		Size: 381.4 KB (381393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaaabaeb5b96837db2cb0467b10175df61b082f7bf82f8a5d608cc48439898aa`  
		Last Modified: Wed, 16 Oct 2024 18:44:35 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json
