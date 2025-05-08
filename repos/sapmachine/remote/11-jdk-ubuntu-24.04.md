## `sapmachine:11-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:c9fb0127d6917dc51e9e103318f5c995a51b73b10ed93c94a6780153db2ded22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:08f4f8e03a47495a65593561d66ff5c87b1dd4d9a59263cb019ec9ec9c017762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230977456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2785781112cb3339e6cf46a0bc6deea3e5ff3b5e419eb1144e7e72eae75cdc1c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223931ed80dd7fd06b1424c4d6e1652663a0bd441a6031ebeadb9ea5615d6fa5`  
		Last Modified: Thu, 08 May 2025 19:07:11 GMT  
		Size: 201.3 MB (201259927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:82009e3cae3e30bb745b08648d6971a891f515ed33f370654e9e63bcf2a986f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f3aba8f6e85960eefb84a67b0bb16c4bc38b6bfd8547bf8ed4d243cc29136c`

```dockerfile
```

-	Layers:
	-	`sha256:ccfa077cb8d62cd975e642cf3f37e703ad8c96df51f0e2ad4853a3b41f86e73e`  
		Last Modified: Mon, 05 May 2025 16:37:21 GMT  
		Size: 2.5 MB (2482929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3089e22ec3119dab013e7085f874534de58544b12acda0c023672678f07606`  
		Last Modified: Mon, 05 May 2025 16:37:21 GMT  
		Size: 11.4 KB (11393 bytes)  
		MIME: application/vnd.in-toto+json
