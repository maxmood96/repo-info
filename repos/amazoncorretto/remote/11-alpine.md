## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:35da02147b53bd1d14f826398d49b818930dc68ee5f642ee4e58e8e3c81caee0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e92c29e42f773314f907cdb5f68f8ddfcad9a0bf7685ee22ef7779a6d6830c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145553055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728a11f8b7b3f4a9c2421a0f80667fe37d9b9aa39a65c836cf4d01e64871e04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a059f3ce0567c0042e0652027140bb7c6432621664cf63f63f3bac27a3dbb5`  
		Last Modified: Fri, 14 Feb 2025 19:12:37 GMT  
		Size: 141.9 MB (141910808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e24fd63a27271dda47444149c47a90883738a313b3b56f4d38c77f8793a5ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aeb575cd45631dd399e361fe3795aea732c7f9a66447a232f97d1ce231d382`

```dockerfile
```

-	Layers:
	-	`sha256:2b25d80f636a813e7b6918c1fb5391280fcef50930e066552b561d8b72947de0`  
		Last Modified: Fri, 14 Feb 2025 19:12:35 GMT  
		Size: 390.5 KB (390497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec25c69aa67600e464f2928f9ed6585f41e1933f76d670f10f34c564dae7bba0`  
		Last Modified: Fri, 14 Feb 2025 19:12:35 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5231b1b770e5a64a50310e7366f9d3e94255a0241f4267a295420a3de302aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144027924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9adedc5c062e7bb0e0e31eeb88b74dc083fce0fff4a9220c996bb457d640c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f739728061184d90aef9cc5810422af618a603602cbc59ea7c88c7f84a13bc`  
		Last Modified: Fri, 14 Feb 2025 22:35:38 GMT  
		Size: 140.0 MB (140034895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a43a7e315fe95be2cf926e4c374bc9c818221e0e054e0d09e102fd9fd6b529a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c36b18533d17922169e5c3cb56ec2bce46dd1dadced7d5bbda7874d15e3abc3`

```dockerfile
```

-	Layers:
	-	`sha256:d3d1eefd1507cbe925d839b74a3a62ace886e19a80378f9b833ff23a47152acf`  
		Last Modified: Fri, 14 Feb 2025 22:35:34 GMT  
		Size: 390.6 KB (390601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a17e5df74eb2c222e8c8a4cc05847298c28e8782b7404bf57eddf5cce906704a`  
		Last Modified: Fri, 14 Feb 2025 22:35:34 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
