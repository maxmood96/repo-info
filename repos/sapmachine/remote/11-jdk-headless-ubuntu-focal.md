## `sapmachine:11-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:10e6445fc711ab31bb16365f78a7401b9b50eb98eb79e9a9597526cf2ebd7b8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:30124fadebbb67304a71f2bef7a722783ab949d37c4c664dc4c0e718914a3951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226724667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36785115c9c8cfbddbcd8aa8df13c9b182971e3f5a911a925e5b9bcb4d065283`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c490ef822f6520daf78f738b70fff6fc3fa67adef781958afd3fd2495b62446a`  
		Last Modified: Mon, 19 May 2025 16:52:11 GMT  
		Size: 199.2 MB (199214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d36d969bfeb97bdfc444926dad02295b38acf67caf21cf3328901ddb9d3bf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847fd7c019bfd0ee9d38428edaeca0d205da2cf7b59e1ba342e62782de2d5533`

```dockerfile
```

-	Layers:
	-	`sha256:d8abc3aec15547c0af21b1b61f58022848a9d51c12c736259a69bb08aca687f1`  
		Last Modified: Tue, 17 Jun 2025 10:30:46 GMT  
		Size: 2.2 MB (2156849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855a6f48283655f73820e120c290eda5fa4d72fa1026d81879f7023b25ffc185`  
		Last Modified: Tue, 17 Jun 2025 10:30:48 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
