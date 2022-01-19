## `amazoncorretto:8-alpine3.13-jre`

```console
$ docker pull amazoncorretto@sha256:6e54be285e4cbf2e95feb44c2d9c2ffc4a60da0289305e249c16c7b5732e7760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.13-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:faf19cecdc669402d5719a74c04c27aff6225c919473503546e9a043bbf2ae8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43194409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01abd4a2523408f4865276e1e7a0695edeaf11b97bd968e9048807b8c17ba283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:16 GMT
ARG version=8.322.06.2
# Wed, 19 Jan 2022 22:02:34 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 19 Jan 2022 22:02:35 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:02:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c90b0eafe6cdb26c97a65c691f1b6c9715526b5e22c3ebe7b5c3e95103f8449`  
		Last Modified: Wed, 19 Jan 2022 22:08:15 GMT  
		Size: 40.4 MB (40371984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
