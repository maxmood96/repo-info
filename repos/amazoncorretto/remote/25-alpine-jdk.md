## `amazoncorretto:25-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:80667e38af71ac103a3ae36a0b531d54c73c4da28fc02b57f69bce8993c0e1b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:82b47fe5eca3bed03ade22bc635a456fea623d36bf2c0d217fe9b3c686fc7dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184863169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1787148cbd587ebe9d35fa38011c108f6dfb7101380f8766ba29e665060e6ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:23 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:23 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:23 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130299703f5831bc35b5254b4eb5549c81fd91109769f9225c20dd65844ae64`  
		Last Modified: Wed, 22 Apr 2026 21:35:44 GMT  
		Size: 181.0 MB (180998980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb4f1d8789f26a2930af1e7e3a22dc5247c4935cd5ca98994af24f90308fee1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.5 KB (603483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357a17489e1b0ab9d433d0a7988add6ee8fbcd072d0c3d6072e3d86668107168`

```dockerfile
```

-	Layers:
	-	`sha256:47eb84e531428fa7d8b334ee34af8d0fdcc3247553956fdf6d4ed1d792e12245`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 592.8 KB (592806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c5059fa6f6f86ff7ebf935ace7773575c74754ca1009c8224d1460eee35d4e`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b1d413d642474782437d8a92c7fa538f6470fa6fa1afcb18efbcda058c287fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182821669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586661f3deda172699e5bdc6e9bf109efe3d137a7e0e35648263779ddc20bb7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:17 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:17 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d236e04af56142e3286d8350a8586b6e1a108498823e2f4b6b22a514d970c21`  
		Last Modified: Wed, 22 Apr 2026 21:35:40 GMT  
		Size: 178.6 MB (178621799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8dc20149257b650ab4c669fb52d8e1bb35e133f8b3f7bc630220aa977d313050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.4 KB (602449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0412a9601db0cb1184938f15d1a1cbe2b5d549239afc04897b23d09526848072`

```dockerfile
```

-	Layers:
	-	`sha256:94e353e0d10ea0925e38a15cfd72ca3da6ed406d52a58d8bafde14d1032f9e91`  
		Last Modified: Wed, 22 Apr 2026 21:35:34 GMT  
		Size: 591.6 KB (591620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de08aeb827db9a4b3c28c7394290d42f01138385c197d9d6bfd7e443d3bec6e5`  
		Last Modified: Wed, 22 Apr 2026 21:35:34 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.in-toto+json
