## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:2e9e4b83674b164280f75dd94ece76296e5b35d278d536ffdbc3da9bb868bc83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6516305520b0f913120e327b8757ca320d40f95fca50be08c23e8e257b424474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d782a33f1d245132d3bd493c0227529807add0c60fc8e6dff835dada3e7d2c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb33e490e80c5dbfe894c6ed65790c947f7c75da52af885757f1b8562e3ddb42`  
		Last Modified: Tue, 02 Sep 2025 00:22:13 GMT  
		Size: 50.0 MB (50007074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:88e0bce4b3ba5b6fa205539838b0f090d2a4ff0abdf4254c1b0c707172971b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da3e35284cf0a0e35945e3c9f5135dc8a27e19cf753c48b535311a680dbf40c`

```dockerfile
```

-	Layers:
	-	`sha256:01db9ccd27368c488b0ea40446abc29d7958e1618d426b6e9861326aea0b1396`  
		Last Modified: Tue, 02 Sep 2025 03:04:48 GMT  
		Size: 2.5 MB (2549886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055bae3139a216d11872fe7672da6e363efe1257bb5b2f6a7b394c4d3eb4b452`  
		Last Modified: Tue, 02 Sep 2025 03:04:49 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json
