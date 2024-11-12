## `amazoncorretto:11-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:6bba7c1ad1a389843fa6a4134eaea318ae8f67d9d112cbb9a2c0c6e91cec4340
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8a2081988890cb01ff6f47a46b4d09a42371ae791164ffe5f61d46c76fc02d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145326766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13ba093f792a5f8e815abf51c0a16fffbb13d69ce835b597a1fccb2c854c5ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d803ba34e3c1b3ae95b37b3dc251f08eccafa38060ec176018d6f74223c343`  
		Last Modified: Tue, 12 Nov 2024 02:12:11 GMT  
		Size: 141.9 MB (141910365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc979a55763eb7d01f7442bc1d0c754987b2bb38bb683fc02fa8ade7bc2364e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eeca29ac1117bb04265d7a10255cd7578895eff792935b35d21cd1080fe87a`

```dockerfile
```

-	Layers:
	-	`sha256:845fb7bcf8810da0874d016ee6473c98e991c899b2adff48933d8c56ebb86ec2`  
		Last Modified: Tue, 12 Nov 2024 02:12:08 GMT  
		Size: 387.7 KB (387670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ceca54d545b382e473c1bf33e9b054c719d00e6517d6ba32ef3cf14896564a3`  
		Last Modified: Tue, 12 Nov 2024 02:12:08 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:98a788daa18a16698d4c46c498ad4b38e53d410333ca2383c47e50340f29d29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143371464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a731162710e1992483aedc0f4949dfd23fb5a1932966b178f6356b9f46e53db8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d54a1e633eb2f34783780aa306e9b4a955397f42f84aaeba55024cc5d39c6a9`  
		Last Modified: Wed, 16 Oct 2024 18:17:54 GMT  
		Size: 140.0 MB (140031117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fdf11026dc412686c2f4862db38f4a08203034e6bff74b47a682787f7296346f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 KB (396941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ae5c20aa127fecb208d7c5d56e6437ee7320d281a0bfe044fb43e40682bed0`

```dockerfile
```

-	Layers:
	-	`sha256:baf23bf4155b031ab28253ab5dbb6e547e5b8f64aeb92777b18d30ce23096862`  
		Last Modified: Wed, 16 Oct 2024 18:17:51 GMT  
		Size: 387.6 KB (387633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212117bee390df277c0813e914c16b5e6f5aab4bc3b50aec576e6d928372326a`  
		Last Modified: Wed, 16 Oct 2024 18:17:51 GMT  
		Size: 9.3 KB (9308 bytes)  
		MIME: application/vnd.in-toto+json
