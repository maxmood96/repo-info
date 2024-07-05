## `amazoncorretto:21-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:3166585364e8a79e82df26289c13a885b33e7a1248c50a81362feea3e398b2d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d47aee83991ec3ff1999a34bea1feda8933cc59eb26679e72959ae3e19e7a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163264437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2b1f2439ffbf62df1700ac9907e7d25e8cc3958e6766dc1f21ade2e817446d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fed50077d698511463c6f380abf47db55bc9500c95a56b0de8d1ac74b867db`  
		Last Modified: Fri, 05 Jul 2024 19:56:36 GMT  
		Size: 159.9 MB (159874474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a53c26ea93470a744116909c3c0f0462b67b78b247c2f3c8175fdb41f092788d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 KB (385197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2ea10642d2ba6248596b6978ad84e106397d42cd5a97f06a06ab54b93442e9`

```dockerfile
```

-	Layers:
	-	`sha256:6bbac2bfb483376aca08775302df139c26bbd1a6a1ffe34a1eee45f54c58c98d`  
		Last Modified: Fri, 05 Jul 2024 19:56:31 GMT  
		Size: 376.0 KB (376028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6768c43822203c01768aac06144564354f648c7929c7dba56878680f121ca0bd`  
		Last Modified: Fri, 05 Jul 2024 19:56:31 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fda281ff58bf15614d898c84159457bc27e65fb145fcad5811626dc86c6c47af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160660177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f9e6cc066dc47bdff00a85fb4be5022e8d4b56fe16db5696c6b972162df185`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b693b1ba08de22ca63f96def59c3f00418078e3318d57729f5b665c3dc82a23`  
		Last Modified: Fri, 05 Jul 2024 20:25:40 GMT  
		Size: 157.4 MB (157387591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:08d91b939b1f2b22f4b357fe6851bed358c95cc79623a6a1280337557987813c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 KB (384915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa897e816127fbab6df9643cd204dfd7b830d2230f1f4a05b0fdf0f232c56e8d`

```dockerfile
```

-	Layers:
	-	`sha256:4c6408c032c58d251c75a6593aea2049353197fda6fae7cc47fbac6d899ce278`  
		Last Modified: Fri, 05 Jul 2024 20:25:37 GMT  
		Size: 375.4 KB (375446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6454a9047cb79edd1072f1f23b3df35c52ceb192a648f679f40dc5d54f0200`  
		Last Modified: Fri, 05 Jul 2024 20:25:36 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
