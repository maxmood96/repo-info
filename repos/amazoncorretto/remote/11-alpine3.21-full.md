## `amazoncorretto:11-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:18f6be99776289990f54db75a4a60fe5176723752de272ab60e155be31130762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:52f80ce1d471f0b8dadec1d21577dc634ad6146d33d5e8094479bc29f0361831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147229901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fc76c71368ad9ba50ecb7681e40e46ec5bd95128ba964e087e9aa0674183a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
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
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba62b8026c3b93710c6fc1006b2ae547cce88a4414273f32278ba7cd7c43ecb8`  
		Last Modified: Fri, 17 Apr 2026 00:22:47 GMT  
		Size: 143.6 MB (143583026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:587eb6297eddcc3f76a64b6dfd380c412c471d859787ab10e821d4baecd6dcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 KB (602737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447ddf31bd27544e7beacdd4178af3d28f22368d8f3d848cfb7e793bba301e8a`

```dockerfile
```

-	Layers:
	-	`sha256:6e9277fa0ee4acb5fb33468c01228c131d811993f9d763083bd9305b9c548334`  
		Last Modified: Fri, 17 Apr 2026 00:22:42 GMT  
		Size: 593.4 KB (593363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f19edf722a1de19be268c45e8580f4fdd6785f0d4ba032950905548684cd50c`  
		Last Modified: Fri, 17 Apr 2026 00:22:42 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c0689d29a4f267d5cbd5b0de26f2ca956a825807a40770f633a3cc2d1c405d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145842445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fad0599cc128d2a2bf2726653e33f2185277e1e30948e78f8dcf6a3cd342562`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:35 GMT
ARG version=11.0.30.7.1
# Fri, 17 Apr 2026 00:24:35 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:35 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba440e9822d7a143d7807d7a90e96bbefcad104c5376dbc075c7968ecfca73`  
		Last Modified: Fri, 17 Apr 2026 00:24:52 GMT  
		Size: 141.8 MB (141847980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:43fe19448999f9107630ad03f5be5ef7a64b9084a640723c7b8117202d02dd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 KB (602897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9babaf87c8d4d9045d16a1974896551a4c32619f5c231f8987581077a699ff97`

```dockerfile
```

-	Layers:
	-	`sha256:108e8697862de17450664163d8604323cda2a4bd33d9badb96c31f70932b9ec7`  
		Last Modified: Fri, 17 Apr 2026 00:24:49 GMT  
		Size: 593.4 KB (593419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc03932630ce17bbe5f61fe795137083d0b2f2be7b71aae300e24bb537b7a58`  
		Last Modified: Fri, 17 Apr 2026 00:24:49 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
