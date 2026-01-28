## `amazoncorretto:11-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:23f47739ab91f05236fe03203fd81e07c0f9df60b603d52a9e4023e8dd1534a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:beae1c75d05e6c7fc410bdcf194b793c0a7cf3c16333e81db54b9d8951c3c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147394627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafbcd7967e582b7888943b5defed30650488b4ea6f85f717c00bd706f1d1ae1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:54 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:45:54 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:45:54 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:45:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:45:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8837d612de9dcbdbac2596daec96b61b87a34ec893f8c6ff685184af55bf82`  
		Last Modified: Wed, 28 Jan 2026 02:46:12 GMT  
		Size: 143.6 MB (143589752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6684ad900cd1f8745dcad62b9ef62c818498eb5380d00bd55eb520ce0ff8246a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0eaeb820964e32626e05135516237acdc9006b22c918a27056306dac1f5f9f6`

```dockerfile
```

-	Layers:
	-	`sha256:ed6f9973c2a163ac32502fd9cd40c9fc87d0ddfbdae7a3f6955a8ffb9cad7840`  
		Last Modified: Wed, 28 Jan 2026 02:46:08 GMT  
		Size: 588.9 KB (588928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89783e3b7619f5a74e45087804609673c8349cd4f67880c81be27e0384f1577f`  
		Last Modified: Wed, 28 Jan 2026 02:46:08 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:20788ea1aefb0cd4663abf2225a40d1811f464dd3755df2842b521d1c3302d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507596c46920fd28f74cb1a45617fc6508a719f468a20f21e1e86e1231cf5db2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:10 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 19:00:10 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:10 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e383c1903cf3da6da77b9d246d184d2e1d665a7dbe223a71da5be89169745450`  
		Last Modified: Wed, 21 Jan 2026 19:00:27 GMT  
		Size: 141.9 MB (141854400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de4e8be96d4258354255c337285954fd6d0e1f5054f4e616ab3534c3f0b7c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41fff6824728af01eec45b17d070fa421367bd096770fec47a62e80d186aa93`

```dockerfile
```

-	Layers:
	-	`sha256:5eb11a231fc84ea9ca4845d66896b9dcd7b349eecd2eb407d0772088eddfd12e`  
		Last Modified: Wed, 21 Jan 2026 19:00:25 GMT  
		Size: 589.0 KB (588984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e687e9a3b86a435d94295783160215146f983a44f12fc56b58c9a7ae6ec5ad`  
		Last Modified: Wed, 21 Jan 2026 19:00:24 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
