## `amazoncorretto:17-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:abe5c3e006e5235439b43a17fb93db765f8bc6ad42b776804b23ab6b1c2016c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a84ce2027d48b15932c0429beb8e9b7f93fadb1263936287bbb5cb8d0ab0b597
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194630550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff336463764e45422837d39ff8638d96dae014155d263440078e3e8d76b5c3b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:38:09 GMT
ARG version=17.0.2.8.1
# Sat, 19 Mar 2022 00:38:18 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Sat, 19 Mar 2022 00:38:18 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:38:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:38:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fbd2861622eca8509fee4d42fd868b5a252481c85895230ff86985c91f06de`  
		Last Modified: Sat, 19 Mar 2022 00:47:32 GMT  
		Size: 191.8 MB (191814381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
