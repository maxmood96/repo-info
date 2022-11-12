## `amazoncorretto:19-alpine3.16-jdk`

```console
$ docker pull amazoncorretto@sha256:46be4d85ae0f45ee7144fcb0d785907b960ee273f6e3d759b6e0c39bf03e5387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.16-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ab732175ab5450bdc902b4b43661b967cb514b656bdf770d5edd2178dcda5f7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203284336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafe5fa866d9e361a48a23f5994d970d6285859d4bf6a706f275b09370c981d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:55 GMT
ARG version=19.0.1.10.1
# Sat, 12 Nov 2022 04:37:03 GMT
# ARGS: version=19.0.1.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Sat, 12 Nov 2022 04:37:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 04:37:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 12 Nov 2022 04:37:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b953496144a820faf3b5884ddfc542a98cc07f6a24635f26015e7c8d0ef19efe`  
		Last Modified: Sat, 12 Nov 2022 04:41:48 GMT  
		Size: 200.5 MB (200478064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
