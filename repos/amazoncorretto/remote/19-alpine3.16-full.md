## `amazoncorretto:19-alpine3.16-full`

```console
$ docker pull amazoncorretto@sha256:7949de351f5378500ded7e0422f761086c8d290e51e6d015a789ff54317b6fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.16-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d4c27f0baf8129a1cb149d9fd63aed7a0fe9f85d157ecaa1f2e399e8d3f5ed0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204894602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba91d69b6efd77c20bc9be22a1d6f13462ad78e42f9305e22a1f4de73f95d4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:01:32 GMT
ARG version=19.0.2.7.1
# Sat, 11 Feb 2023 07:01:38 GMT
# ARGS: version=19.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Sat, 11 Feb 2023 07:01:39 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 07:01:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 07:01:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c161729f2786ef22ad02911f45591d1fbbcb58086c3ecff7467ab80f80f86f9`  
		Last Modified: Sat, 11 Feb 2023 07:11:32 GMT  
		Size: 202.1 MB (202086840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
