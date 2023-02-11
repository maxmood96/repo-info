## `amazoncorretto:17-alpine3.16-jdk`

```console
$ docker pull amazoncorretto@sha256:6c079b743be467b99af10f904ce654496e728f089c276d6e974c24bfe79749d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.16-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e14741529d98cf9ab4d1e6cdc1b237c21c7f4037c2454b7ddaed8d71a0765e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196377550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a62715804514a0492e2aac6df98ef2e10491cbeb2bfa826c5f57e619f65924`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:00:46 GMT
ARG version=17.0.6.10.1
# Sat, 11 Feb 2023 07:00:52 GMT
# ARGS: version=17.0.6.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Sat, 11 Feb 2023 07:00:53 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 07:00:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 07:00:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c952d2dcba6006dd6a1fc5b4b4af53a277b0ad9bea3ebc823f54d876437b6`  
		Last Modified: Sat, 11 Feb 2023 07:09:28 GMT  
		Size: 193.6 MB (193569788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
