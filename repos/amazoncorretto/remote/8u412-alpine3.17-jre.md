## `amazoncorretto:8u412-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:91f50a87eff28ce56ff7d28c1638775e00baa11e34ff0e6fd2e38cbcbc56b75e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u412-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:584673a0c512e8fecbeda1cb8e863b2a1dc795be6936748670cccea00acdde23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45037608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542f85c8d91bf293fd64f699dc772c723b9f61b2b5813c4ffb67aee903df2ce1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e287e6e5ca043f37e0b65bf77079bc52b01ab57db940a3499cf72c51c1199e0`  
		Last Modified: Fri, 05 Jul 2024 19:55:58 GMT  
		Size: 41.6 MB (41647645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u412-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8cea0c6b1566b467b8bc9481814513ed83663346f90f12a81ecf2d9acc293201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 KB (186630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45379f512f3acfdf1fd4c65668aa8abec266b69ec29b98ad1f28200664dba0b`

```dockerfile
```

-	Layers:
	-	`sha256:f3e79f2fce32bc41943396931d9911fe0af7f43355371964362b300fd2d49784`  
		Last Modified: Fri, 05 Jul 2024 19:55:57 GMT  
		Size: 178.2 KB (178176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e508664802c4315f7c4f21525da5bc84c51b78833ab024a4dd182413baec35`  
		Last Modified: Fri, 05 Jul 2024 19:55:57 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u412-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18529dcde88ab00bafa96bab2d98ce05576ee3fc306fd128a2bf94df277bee92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44572669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7584fd037fef62c333e09842fd450df96dabeb51e0269c3449ddf59b595a0e85`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68ef473de5a8f8c7cae52cfd59868672b555b21a8a11e56c5de9f3e4637789`  
		Last Modified: Fri, 05 Jul 2024 20:00:40 GMT  
		Size: 41.3 MB (41300083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u412-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d739b97ce8e1ebc5541fba318708667e8da35061cb91fc9185ec95e429dade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 KB (187014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893e5c56cabbabb9c4af7c84cb5424d3889d5899d69fa8207695e2ff49470d6e`

```dockerfile
```

-	Layers:
	-	`sha256:d634d3bc6a4599c29c05cf33e49047bafba2192370c786e08866c24cd737cfdc`  
		Last Modified: Fri, 05 Jul 2024 20:00:39 GMT  
		Size: 178.3 KB (178284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8238f32017125a129315046d1b6c8c8f240b0925e504cab1a179b32adfc50ee6`  
		Last Modified: Fri, 05 Jul 2024 20:00:38 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
