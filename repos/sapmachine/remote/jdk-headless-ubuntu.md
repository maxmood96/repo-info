## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ca6d35e79706468db7ca42d6545a614d6a866bbb4dd5447cf9804c1dd504fd87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:24ee21b6c9b3daeba07b777eb2bce940f06e825929cbd5bc1d1e538657c010db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260975548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93b8eb9a9f5a9fb6cdba6758377cfce27317001d7eaf9b3b1b5b8712af4c802`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502f314a3e4ebf1c6b3c001b5bab30b38f64b7b74cdafb8a0eb53154b55f844e`  
		Last Modified: Mon, 05 May 2025 16:36:50 GMT  
		Size: 231.3 MB (231258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:094c8b7761b599c12de9578e1c0bf006a98647b338352b2f42251a622ce27f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518582aca0165fa29e836cd44f5594afd220452e6ff8e99b58630a0a1de9406`

```dockerfile
```

-	Layers:
	-	`sha256:fb496d656f5d30ce07bfdb32bfb3d39f5a7b6bc9a9c828aad20f6f5e8dd2325e`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 2.2 MB (2225211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb9198ce1ead9fb911f687169d04920b958c1647f557f9eba91ed5fc47282b5`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:97c0b4e2d83fae7c6789400fc80bd84920b5cb885ce072f4ecb72d4433acf3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258012553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2d0637d1b87f57c232260702dd88ba98d763f7d37d8d594c23543ea6aa112c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d5cb829c802ac31c11a630ffa933cc83bef494bd5f642f10345be5205fbdd`  
		Last Modified: Wed, 16 Apr 2025 16:14:53 GMT  
		Size: 229.2 MB (229165595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:790cd46cbeccd86033b7b0dedd8b7e6dc1f2dba08d6fb23fb0586fab732331c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082981f7accd7599075dfe3a788a3c192a209d3b3551b62a580468b7b5397af9`

```dockerfile
```

-	Layers:
	-	`sha256:41a10ca6585077cbba7402193c04c18c8f5ce7e52281004669729ca2679bf8df`  
		Last Modified: Wed, 16 Apr 2025 16:14:48 GMT  
		Size: 2.2 MB (2225723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf302dfb222e1b789da70d4622dc125dedc295160e62ff6e8b232ccf88dffe29`  
		Last Modified: Wed, 16 Apr 2025 16:14:48 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4574efb27bb3edaee6519cb8483754a3a5e3e89882b7e1d155bcbb72743c2065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266717865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e2d40b20fd410e378c2320b8528f5096616cf0722c355e3d9aa7d58e014145`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58b251e8c2c5b287448b91f444dd3eafa22e2fbedad65b408f4393b06f9f16`  
		Last Modified: Wed, 16 Apr 2025 16:17:11 GMT  
		Size: 232.4 MB (232376998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea2acb23167c1ced4cd7a211731e7a485a6a630d295db4d9b230264973196846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0b6fd5ae17d180700a32e329f82f68067d204f1f19cb4cd1a4312a465abf45`

```dockerfile
```

-	Layers:
	-	`sha256:0eab5b6d2b428ce24ff12fcb276bca6e9359a6663ccac5ab47b81562798c6ed3`  
		Last Modified: Wed, 16 Apr 2025 16:17:05 GMT  
		Size: 2.2 MB (2226549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9768dff0bc700b0ab74a83d3db94258a3f5e03635f20fb497c1bc0859788e1e6`  
		Last Modified: Wed, 16 Apr 2025 16:17:04 GMT  
		Size: 10.7 KB (10702 bytes)  
		MIME: application/vnd.in-toto+json
