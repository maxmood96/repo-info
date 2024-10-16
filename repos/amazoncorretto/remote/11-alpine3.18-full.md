## `amazoncorretto:11-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:02e6cffcd5ba1c4a6ca653215e11a68912f6b8ced6158d657d83a04aeb98a29b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0279d7c061b1e63c3ab96b066af06eecfc5b84df334dae2eb6f266bd92ef7143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145326489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c545d0638ec1c9664bd2bf866455fccc73166c48ce812c2e56373a8de4c3ff93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:19 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Fri, 06 Sep 2024 22:20:19 GMT
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1244f279c2d94add48a62747267924ac7f52be7411164de760903fb8283f687`  
		Last Modified: Wed, 16 Oct 2024 17:56:09 GMT  
		Size: 141.9 MB (141910176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:55d32e81ab540bab3ad8891f8015284198d1afc7fcf49a0fe9199df9642a0a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 KB (396787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541a9f8e671175826ed0c2510965509bda1277ffd9a462e71d60950b8922628c`

```dockerfile
```

-	Layers:
	-	`sha256:2421e997373805e09f0b69efe4af05afc35853e1d05e00802d35e7804c3308a4`  
		Last Modified: Wed, 16 Oct 2024 17:56:07 GMT  
		Size: 387.6 KB (387577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11c0c733404ceb663b9c7a5f6d8d37e5ba94e78223ccde84d7781517cf6e1ff`  
		Last Modified: Wed, 16 Oct 2024 17:56:07 GMT  
		Size: 9.2 KB (9210 bytes)  
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
