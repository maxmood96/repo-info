## `sapmachine:11-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:4949081d53fde732cfcfb98b65178865719815fd20a5eb3759df6de46b1443f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:51ede5a99db9cd97893e55491ae8ffbd72bede00928f04d8c870fd8bcb1c6e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229178912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031cff63b0212ab40a8414a3b1ffb894922c87403e687c413a4639f56a6e362`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:46:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:46:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 15 Jan 2026 22:46:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4300f235ece67ef441885234528f1354f826a8cf7e03df6c1285cd0ad93d756e`  
		Last Modified: Thu, 15 Jan 2026 22:47:07 GMT  
		Size: 199.5 MB (199452901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a309030f2887bcc6d98156baebdcfb5102f8602f658a91b7d0ebeed5f0c74b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985dd0fe44651af5edf158b4a57615cacfa4887ec3da1fba1cacf19317c829f8`

```dockerfile
```

-	Layers:
	-	`sha256:d87b3f99dd423f7238ccfd163c3342afdd50556f7c9c6aecfa905a48dff55e96`  
		Last Modified: Fri, 16 Jan 2026 01:05:40 GMT  
		Size: 2.4 MB (2367224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fb5f4a5fa747361818cc96221fea05bafdd4f55703ab0f72a17066db8e8fbc`  
		Last Modified: Thu, 15 Jan 2026 22:46:43 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json
