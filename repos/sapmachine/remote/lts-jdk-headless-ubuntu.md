## `sapmachine:lts-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:71c3e0e9071bfdcaf8aa7461cb4c24b3e6a52bc684e8db84d4097d1ae1e44f83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:b9b826f7507da04fa2b2fbbd9378f245ae1d9ef0a05294cf461d1bd2f83aeaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250728833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2435fd5c08610e0355a3dc6bd31d5c6375e7ae705607c1021d7f4ea436166178`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f5b79d43e28938aeea9dccfb91747ab8dc02dfac7472431e1704e6bf50357a`  
		Last Modified: Tue, 21 Apr 2026 23:04:12 GMT  
		Size: 221.0 MB (220995855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:34e31e50238746fe1942ca29b2ddb52bafe2fe147a0f7839d563216c082e6fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d660fd2aad09508dbc6d7d5528593ac376757575e97985062a0518c8b815b45`

```dockerfile
```

-	Layers:
	-	`sha256:bddc1a969c3a0056610de6269d33f719eeca7d9e3a5efcb325a34260871dd467`  
		Last Modified: Tue, 21 Apr 2026 23:04:07 GMT  
		Size: 2.3 MB (2349897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f73fdd416e9d4a3417e40d7f11b5ce51146096b279ead3246a7a1b9cfec1e23`  
		Last Modified: Tue, 21 Apr 2026 23:04:07 GMT  
		Size: 11.3 KB (11265 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1622d443217f4846f1db2901cb9f0435339f0a17b10e6eda3606381683bf33df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247668437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f146c2db55be68982d21c03d42fa8b242069d699a8a57c12de20391c523f6209`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:05:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b0f658f291653781bfa832b201844db17c8fc1a5782b594302602e9fb87e3c`  
		Last Modified: Tue, 21 Apr 2026 23:05:36 GMT  
		Size: 218.8 MB (218792652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b519727d3175a6da1cd80c912496126f87da7e1cd752c5ecf22d57011a809259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22a98581a5cecd45daf561c21afbd696644465095dbf98f2ff1dbf950ab29`

```dockerfile
```

-	Layers:
	-	`sha256:336c9db3a5ff665d7a15a4ebcbac14af6316607bff83bedfb194d9642388d09c`  
		Last Modified: Tue, 21 Apr 2026 23:05:31 GMT  
		Size: 2.4 MB (2350437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb7d24924a3cd434d3ec9acdf89b893d88c32bfb206b79425046405f73fd2a78`  
		Last Modified: Tue, 21 Apr 2026 23:05:31 GMT  
		Size: 11.5 KB (11453 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:acfef17a9fb7dad5062f5e633ede2c4911c09c4b5af02d7a26b44ab3665ba3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255826349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b799874d48fa8cd07e409849aa161b24b7a428ad18baf3069081168521e5bef7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:13:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:13:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261bb745bee230cca1c337f3934d788be60693c5478bf824e59f8a97bf357fe3`  
		Last Modified: Tue, 21 Apr 2026 23:14:09 GMT  
		Size: 221.5 MB (221512171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9654c8297e3a6bd688e76fe98501ca103ddb10e04ef9c3614b1ccaf9f38f8f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2358119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690e890346db8fca052daa6e86b08f172f7e2a9fef78a89d9069e414a9d78c1f`

```dockerfile
```

-	Layers:
	-	`sha256:c7924dae1e4691d770da67d5640df15bcfe4838260a0827568670416bdc86fa0`  
		Last Modified: Tue, 21 Apr 2026 23:14:04 GMT  
		Size: 2.3 MB (2346768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3830249819ac729ddbec8c4154441f6d7c26c324e84db834f267dd37f90ca146`  
		Last Modified: Tue, 21 Apr 2026 23:14:04 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json
