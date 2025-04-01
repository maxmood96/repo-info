## `sapmachine:11-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:21ff8c6d9a79cadbf0f9eee76c153243a677f46ec0a9c476a923be20fb1dad65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:98a5391956428767f900fa53436d10f78411b7de90409c8040d430a580ae54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226696192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e227a243290f555c36c85981525b9ce59d35b6c8ba7cb6366a9808e753364f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977344bdfd557d4ee640d0ad41e78a01d41bd64f8c708619f76dff0f92bc39c`  
		Last Modified: Tue, 28 Jan 2025 01:30:57 GMT  
		Size: 199.2 MB (199185132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f063be314531c0249776718d2c450ff6decb163d80d60f5662d89c1f47d7ec36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bf5b0796f1e746a0f536cafe8e9fe69fe4c8dc655bc0d1e49294927b007956`

```dockerfile
```

-	Layers:
	-	`sha256:6acd91976d45bdc340f5a223d156bca5a0f8961034bc37c5d1beaf04dbf2a44c`  
		Last Modified: Tue, 28 Jan 2025 01:30:54 GMT  
		Size: 2.2 MB (2156783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a535a32de38a1af03acc49c0f1fb14b5b772d7b028ef905e01bd884d5e8bee`  
		Last Modified: Tue, 28 Jan 2025 01:30:54 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
