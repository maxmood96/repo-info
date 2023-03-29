## `amazoncorretto:11-alpine3.16-jdk`

```console
$ docker pull amazoncorretto@sha256:b2bc7c24d17fa74789e04d35b47809f8eccbd17a672d2ba46bd5eac5d0e337ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.16-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55ef3ba7ebe706586d55610f4b520f26fbbdadec08e01d364ef41a2d910dc29d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197941346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f5096065a61889c85ed91468695c9daf336950d143a299fb9cb21ec10a76a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:18:15 GMT
ARG version=11.0.18.10.1
# Wed, 29 Mar 2023 19:18:20 GMT
# ARGS: version=11.0.18.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Wed, 29 Mar 2023 19:18:21 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:18:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 29 Mar 2023 19:18:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bf3d7ca47d5ca6a174fd7e46ff6064f91538476839273cd4ce053092a6dca2`  
		Last Modified: Wed, 29 Mar 2023 19:24:57 GMT  
		Size: 195.1 MB (195133543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
