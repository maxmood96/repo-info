## `amazoncorretto:8u462-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:93f3137db91fde470b39fff320f01941f47d2827194d8a143d5755e9c9f677af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d2276491d2c4026447410d4a7527b9804e9bae29163778e6a5656383e4120ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103714967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca9b0d545ca1b05a81012fadc467bb424af258b8d0b82748710f3c2630fbdc0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f36322b317f36dba2d356595dbbd83a55340ac54f6c598654100dbfe6c9fc8`  
		Last Modified: Wed, 08 Oct 2025 22:59:17 GMT  
		Size: 100.3 MB (100295152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7abba62b6b16ae5d29694340153473be2c5521d982e38a03abec88bd111acb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 KB (256800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a78e09e35003b134845c7fff947693f7a1a1f2b47e4af253ddd8a1c292d6b2`

```dockerfile
```

-	Layers:
	-	`sha256:7d9ed55528b40d44750b7adb0489a43f4a2a30a781aeb65999c6f4dd329e9cf1`  
		Last Modified: Thu, 09 Oct 2025 00:53:09 GMT  
		Size: 247.4 KB (247402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01dd3800c74a9a4c2bae219a521c36f1f51a821f41409c75a9581ce98f58cd68`  
		Last Modified: Thu, 09 Oct 2025 00:53:10 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b912708f9826328f7048e29d6b64a9e2e177a90cefff2ddcf2311e2afa0ad001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103451374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde6111cdaba0a03ff2016cb6203ad2914cf8a9c8dfad93ad2a31ce3cffeafb1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861c46243e985558a5c79dd4453e232cf446e6321a45e04196ea0e23a0e3092c`  
		Last Modified: Wed, 08 Oct 2025 21:46:18 GMT  
		Size: 100.1 MB (100092073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba5bb183f704263717dff260e83849fe325e7f264601d1a5cb1f27761a56f8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e33734a80b715c15869f734f5a6c25e007731cdb56d96ee9492a9c10e2e94d1`

```dockerfile
```

-	Layers:
	-	`sha256:6f708dfcb248d50c595a15f9d76c1819f4df38f90c3bf0c9679fea3720d4bc60`  
		Last Modified: Thu, 09 Oct 2025 00:53:13 GMT  
		Size: 247.5 KB (247534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a56b640288ff59e754dfeec6547e5b9dcb837e576dc390aa5046c71bc39190d2`  
		Last Modified: Thu, 09 Oct 2025 00:53:14 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
