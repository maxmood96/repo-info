## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:d96f231ec04495e65a0ee574bfa8c3fe688f832ea1a4f0f2ae740e04fb067c3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:869c463bb5a3ba40bc64a96c8076f7a1ce0c7e8751686b72c730a131fa2e319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229850836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cc37440aaf4f97538e9dead2c694ea767d7c4de5d8508d1aabeacfa0a0c76a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd82002f1f7ae2ac79f8854a75be20ecbad5d0ed5cdff204b91128b7bfba73`  
		Last Modified: Tue, 02 Sep 2025 03:04:26 GMT  
		Size: 200.1 MB (200127772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0cee86415321cfa315d716eb88a81114c24a02f50a82669c556bf428273d76dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff0a8bfb5153e73b7fe185edda2e61e281eb07e58d1c28560d5dc94b0222919`

```dockerfile
```

-	Layers:
	-	`sha256:e7e8d5e9f61a07fa2184008f37dae549d1eadf9882696ade83c1d8fb2ea69f0d`  
		Last Modified: Tue, 02 Sep 2025 03:04:19 GMT  
		Size: 2.4 MB (2367208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32c6946964c7780db83bfb956b6af61925f06f0a88de1179c3ffce52acdc6ae`  
		Last Modified: Tue, 02 Sep 2025 03:04:20 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.in-toto+json
