## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ebee2af223b4967802b6b7f193e209562af798cfc7d8324639860ef6aeefa081
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c6470b6d7dd77253f5c283f74bad93934d5b7fae7cc8e4769c5390dd6f2707ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229783034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29d02536d3f3c24a56bfcd62e9da30924ab67503a2f659ab5f554ab16fabc0f`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ca9daecb060d1fe4b91296783ffa167e721f2255a9756db991b0e38bae1ce2b2`  
		Last Modified: Mon, 05 May 2025 16:37:10 GMT  
		Size: 200.1 MB (200065505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a08ef9557a9dffbbb27414ae506f544013022955d6f9822021c102761f159438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac16fe0023b5c303970eddb823ecf4a5c5db3737907133716047b1c4a51b3ea0`

```dockerfile
```

-	Layers:
	-	`sha256:5ab1558dc00e9cd0e0a2b05d5760c170c1ccc5f2f838bc7e85285ff9f660228f`  
		Last Modified: Mon, 05 May 2025 16:37:06 GMT  
		Size: 2.2 MB (2244119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae922be45c3269fd35d01a0fb924c47859fc3cd369dac8ea0776dbc51c7439d1`  
		Last Modified: Mon, 05 May 2025 16:37:06 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json
