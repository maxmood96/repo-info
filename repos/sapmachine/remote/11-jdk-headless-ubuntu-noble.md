## `sapmachine:11-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:563769d152a5893d47ffd2cd9213e965cdb819ff619a216b5f58b44d2a395350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:d208db2b097cf88022faa300bd2a03ccd86ddc9155240ca902369be89be9ee19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229789388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f9d5d6c23c37254163bb9b9941d8f3675cd9f5cc2c002041c7680e651e3fc6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b281393ccc196237c6a8a46cb42710298e26bfa5a5ef70b6e3d6c5c3fdba36`  
		Last Modified: Tue, 04 Feb 2025 04:50:02 GMT  
		Size: 200.0 MB (200035098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b93b02a438d2752a6ee887b64f8dd797a2dae93de10e6d716ee79fad95de2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecddd8afd14fb7a05029786bc94ac550d0ce087dab4bf14df6f673a050750f7`

```dockerfile
```

-	Layers:
	-	`sha256:dcf52b1b36c8cfd06e860e4c17a13bb625c3cdaf6e23002728c78ded03a6e3c0`  
		Last Modified: Tue, 04 Feb 2025 04:49:59 GMT  
		Size: 2.2 MB (2246334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19848d286745356c5f278f69efa589acf54266097d34f972ee32db2adbf288aa`  
		Last Modified: Tue, 04 Feb 2025 04:49:59 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json
