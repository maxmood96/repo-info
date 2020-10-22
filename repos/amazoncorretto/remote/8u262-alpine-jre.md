## `amazoncorretto:8u262-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:9a5333792390874974bcd2b05b0b2d4e98d857373d7709d405977c9e1144ff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u262-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a043d957f7305a03fea58170c2fd2a1f7499065bfb9dc11f7e4f84885c362508
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42195448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe92046c1f14e0a3e6642ee2b56be95e9e74dcc7611c6dc3bfc5d45c982627d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:51:34 GMT
ARG version=8.265.01.2
# Thu, 22 Oct 2020 02:51:53 GMT
# ARGS: version=8.265.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 22 Oct 2020 02:51:54 GMT
ENV LANG=C.UTF-8
# Thu, 22 Oct 2020 02:51:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae1698be12090b1ca24fc27766c9c232f8f7497618f21a389c5d3d6c8ebcdd`  
		Last Modified: Thu, 22 Oct 2020 02:53:34 GMT  
		Size: 39.4 MB (39398588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
