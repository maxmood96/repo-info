## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:5569c63afcbff802389e766a1d7b709b33aa02fd833b03019b1d47b4bae9c1e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:443a0035990d46cbd44e1ac6a959c4f6c75b2b83320d14d32e228354668019cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4995997d42307b892d2edd646f5505d77a746e05d4e1f942b398515dc584ecbc`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7117b0b268f8f2efec9966743e31867ab249adbbafae3b5596275d7d17d632`  
		Last Modified: Tue, 12 Aug 2025 18:09:42 GMT  
		Size: 50.0 MB (50007076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25f2d61529b8ee12fa595fc41ee20cefa97eddf46bd86b04bff82abf160d12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b477aed02b412713bb7e95bef05325aab4dc70c4e335b6839037ea2cb9185ab`

```dockerfile
```

-	Layers:
	-	`sha256:50cfcf87b137586fdb86b4e2c6f7488dddecff1a63359d27a5b27b7cb562c332`  
		Last Modified: Tue, 12 Aug 2025 21:04:51 GMT  
		Size: 2.5 MB (2549870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1bbf5ac0c3cb461a65ddd3269e09814dd931158d4a5c7a09cf5213b23af072`  
		Last Modified: Tue, 12 Aug 2025 21:04:52 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json
