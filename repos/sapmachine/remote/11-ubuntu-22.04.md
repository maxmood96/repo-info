## `sapmachine:11-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e5e964e737df0fd38e19c2bc36d35ec420eca754c8d778b3c5cce0686c6886d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9486e2dc9f5313d07c07eba5d33ea31baecbff2f61a350439794e3c11064d171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230397208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc2e4a951bd09ef1ee3ef07707ae465af6059024269fd5524db48fc13a57493`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff4469dca84081ab347af626593b03c08f332db27cd07f1a7055ac65eb9a6e8`  
		Last Modified: Thu, 08 May 2025 21:20:37 GMT  
		Size: 200.9 MB (200864594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5de4984df1c98cfe2a18595a6eb47d74783274bf11e7d789b79d4c8fbb88f97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5412de2e967c67f6b498ecb08cbcb28f9a43304768df103b59b0ea0dd23de3`

```dockerfile
```

-	Layers:
	-	`sha256:259b6b37007eb00c4cb23da6ebd323c689eb4e3e502353975f20528202730d8d`  
		Last Modified: Mon, 05 May 2025 16:37:22 GMT  
		Size: 2.5 MB (2504193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1737a011a9c810f4b8e737739a641843cd085e460b3356f248621570ffa2c7c8`  
		Last Modified: Mon, 05 May 2025 16:37:21 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json
