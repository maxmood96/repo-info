## `amazoncorretto:25-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:390e7a9ed1ad59b13e9e2e33360039dc30aba8b29baafa7ca37e7e70fa9d03a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5739f8b5049921bb344e67f7aa971d2aa4b02f12f35fdd512cafe5e4930ef10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184403392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bdd6b4a89e8599b786e6a3bc5a53107bfbc6c0090330c09839419056a15e46`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:02 GMT
ARG version=25.0.2.10.1
# Fri, 17 Apr 2026 00:23:02 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:23:02 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:23:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:23:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f190aa1f9c301a6b27ca0f0531ab7c93b9a50c9046b1cefa3963ae9545ff0e40`  
		Last Modified: Fri, 17 Apr 2026 00:23:21 GMT  
		Size: 180.8 MB (180756517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a2ed9a3672e68274536d47b808f748f5c754c3a4dcc4183c380e44c3b2eeae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 KB (604936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd276735614f31b3951d618f41acea98d25858538af2fab346f3c9ca37d3e2ba`

```dockerfile
```

-	Layers:
	-	`sha256:6edd4597c9166958060a8bd49f168ee3a5f6e280ba156b17c3aff336bf4d8442`  
		Last Modified: Fri, 17 Apr 2026 00:23:17 GMT  
		Size: 595.6 KB (595564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c530cd80141636bd74c325892860e3a53c88ea01249a149649e325dd2fcf9d6`  
		Last Modified: Fri, 17 Apr 2026 00:23:16 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6b153f5ccb8e95c9c9dc1fbde11673d21c83b2f424cc8a4ea6d96ba39786ffff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182397438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873de5e46c24530853696c152d523cf62167e0294706111b584bbfabe4a04c68`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:16 GMT
ARG version=25.0.2.10.1
# Fri, 17 Apr 2026 00:25:16 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:25:16 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:25:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:25:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd352a2339645eee91c0fc4dc08107b1d8eedce126eaa37568eac3564a826539`  
		Last Modified: Fri, 17 Apr 2026 00:25:37 GMT  
		Size: 178.4 MB (178402973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:50d93dcc225c84a71364c73d3d21d36c42c56fdb70cf4b4b36dd5ba71d6aba9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.5 KB (604456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943a58f39c1511095186406283954c80ad72ae7d27d43a5ab10806a09bc336b4`

```dockerfile
```

-	Layers:
	-	`sha256:86882e713ab827b0a52855f3bc0d96856bc65c87cb1f1f7fa87ba8b74d112eda`  
		Last Modified: Fri, 17 Apr 2026 00:25:33 GMT  
		Size: 595.0 KB (594980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a94c16a2ec920c05042749c2c9b768a006b05c80ffd1a41af684b419db3b033`  
		Last Modified: Fri, 17 Apr 2026 00:25:33 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
