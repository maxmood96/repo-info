## `amazoncorretto:8-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:afff599c9c63c5e9fb45a27cdc3a5a08443b1b19784a1303e603f2b8e1cfbce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:278d192fddc29f1e54d31a7b5d6735a25d81f2be8857c6497909eebdd164e979
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101616555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b74425b4323661a0699ef455b80720d792782a64efaaf1c6f1965384a4f6ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Fri, 22 Jul 2022 18:20:13 GMT
ARG version=8.342.07.3
# Fri, 22 Jul 2022 18:20:17 GMT
# ARGS: version=8.342.07.3
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 22 Jul 2022 18:20:18 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jul 2022 18:20:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jul 2022 18:20:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6176522f2e730b230cd385f7fe00954ed4151fe20a4f15fc8a846e7fcc8ca387`  
		Last Modified: Fri, 22 Jul 2022 18:23:48 GMT  
		Size: 98.8 MB (98798043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
