## `sapmachine:11-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:90278a955718d33c986efd0a01e2f994503f25b253012537517a35a1e4a7e307
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:f9144bb91316e70b3353da9a94476b5791f90da03116984cb6e1601403d542d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75852169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441f0117c1cef0af05dc4df4fff8dfafdb2305559884336b8dbf178dc767cc9c`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:03da4bc3459484691e17562923b5f5e4a41704012f0df840f02c7fe1baf85fc1`  
		Last Modified: Tue, 28 Jan 2025 01:29:16 GMT  
		Size: 48.3 MB (48341109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:568d7f9c34402535c22190f190956fe21a0c806f0dceeaa9566a901a7e52faec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2076314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e699d7612ccd3d7808ede0d6f18574b7b4f61df0faafe53cd6157452daf2dddb`

```dockerfile
```

-	Layers:
	-	`sha256:e445af96268fc8da3a875b4e2795c64c912a433ac272a40f50665b1349d6a350`  
		Last Modified: Tue, 28 Jan 2025 01:29:16 GMT  
		Size: 2.1 MB (2067382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12495c270a60082e5fe79402e5dcf25a8ef2036d80d41921dcb03fcf7117b4c5`  
		Last Modified: Tue, 28 Jan 2025 01:29:16 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
